(ns silicon.test-runner
  (:require [clojure.test :as test]
            [silicon.cells.test-state-machine]
            [silicon.kotoba.test-ingest-mcp]
            [silicon.methods.test-agent]
            [silicon.methods.test-fab-cell]
            [silicon.methods.test-fab-flow]
            [silicon.methods.test-lot-ledger]
            [silicon.methods.test-wafer-handler]
            [silicon.methods.social]
            [silicon.cells.social-post.state-machine]))

(def suites
  '[silicon.cells.test-state-machine
    silicon.kotoba.test-ingest-mcp
    silicon.methods.test-agent
    silicon.methods.test-fab-cell
    silicon.methods.test-fab-flow
    silicon.methods.test-lot-ledger
    silicon.methods.test-wafer-handler])

(defn -main [& _]
  (let [{:keys [fail error]} (apply test/run-tests suites)]
    (System/exit (if (zero? (+ fail error)) 0 1))))
