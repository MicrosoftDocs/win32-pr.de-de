---
description: In diesem Thema werden verschiedene Fehlerbehandlungsstrategien beschrieben, die bei der Entwicklung von Komponenten für com+ zu berücksichtigen sind.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Strategien für die Behandlung von Fehlern in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca64546683fa45ac8df3bcb47534d8de482798
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344353"
---
# <a name="strategies-for-handling-errors-in-com"></a>Strategien für die Behandlung von Fehlern in com+

In diesem Thema werden verschiedene Fehlerbehandlungsstrategien beschrieben, die bei der Entwicklung von Komponenten für com+ zu berücksichtigen sind.

-   **Gibt einen HRESULT-Wert für alle Methoden in allen Komponenten Schnittstellen zurück.**  Com+ verwendet **HRESULT** -Werte zum Melden von Fehlern beim Ausführen von Funktionsaufrufen oder Schnittstellen Methoden aufrufen. Ein **HRESULT** gibt an, ob eine Methode erfolgreich war oder fehlgeschlagen ist, und identifiziert die dem Fehler zugeordnete Funktion, wie z. b. RPC, Win32 oder ITF für Schnittstellen spezifische Fehler. Außerdem stellen System-APIs eine Suche von einem **HRESULT** in eine Zeichenfolge bereit, die den Fehlerzustand beschreibt. Die Verwendung von Methoden, die **HRESULT** -Werte zurückgeben, ist für gut geschriebene Komponenten von grundlegender Bedeutung und für den Debugprozess unerlässlich. Microsoft Visual Basic definiert automatisch jede Methode mit einem **HRESULT** als Rückgabe. In Microsoft Visual C++ müssen Sie explizit ein **HRESULT** zurückgeben. Weitere Informationen zu HRESULTs finden Sie unter [Struktur von com-Fehler Codes](/windows/desktop/com/structure-of-com-error-codes).
-   **Initiieren Sie das errorInfo-Sammlungsobjekt auf beliebige Weise, die Ihr Entwicklungs Tool bereitstellt.** [**ErrorInfo**](errorinfo.md) -Auflistungs Objekte werden häufig als com-Ausnahmen bezeichnet, da Sie zulassen, dass ein Objekt Rich-Error-Informationen an seinen Aufrufer übergibt (oder auswirft), auch über Apartment Grenzen Der Wert dieses generischen Fehler Objekts ist, dass es ein HRESULT ergänzt und den Typ der Fehlerinformationen erweitert, die Sie an einen Aufrufer zurückgeben können. Jedes **errorInfo** -Sammlungsobjekt gibt eine Kontext Beschreibung, die Quelle des Fehlers und den Schnittstellen Bezeichner der Methode zurück, die den Fehler verursacht hat. Sie können auch Zeiger auf einen Eintrag in einer Hilfedatei einschließen. Automation stellt drei Schnittstellen zur Verwaltung des Fehler Objekts bereit. Die Komponente muss die **ISupportErrorInfo** -Automatisierungsschnittstelle implementieren, um die Unterstützung für die **errorInfo** -Auflistung ankündigen zu können. Wenn ein Fehler auftritt, wird von der Komponente die **ikreateerrorinfo** -Automatisierungsschnittstelle verwendet, um ein Fehler Objekt zu initialisieren. Nachdem der Aufrufer das HRESULT überprüft und ermittelt hat, dass der Methodenaufruf fehlgeschlagen ist, fragt er das Objekt ab, um festzustellen, ob es die **errorInfo** -Auflistung unterstützt Wenn dies der Fall ist, verwendet der Aufrufer die **IErrorInfo** -Automatisierungsschnittstelle zum Abrufen der Fehlerinformationen. Visual Basic Programmierer haben einfachen Zugriff auf das **errorInfo** -Sammlungsobjekt, das über das Err-Objekt verfügbar gemacht wird. Sie können Fehler mit der Err raise-Funktion und Fehler mit der **On Error** -Anweisung erfassen. Die Visual Basic Lauf Zeit Ebene übernimmt die Zuordnung für Sie. Wenn Sie die Visual C++ COM-Compilerunterstützung verwenden, können Sie die \_ com-Fehler Klasse "Raise" verwenden, \_ \_ um einen Fehler zu melden, und die \_ com- \_ Fehler Klasse zum Abrufen von Fehlerinformationen. Com+ gibt herkömmliche C++-Ausnahmen nicht als erweiterte **IErrorInfo** -Informationen weiter. Weitere Informationen zum **errorInfo** -Sammlungsobjekt finden Sie unter "Fehlerbehandlung" im Automatisierungs Handbuch.
    > [!Note]  
    > COM erfordert, dass alle [**errorInfo**](errorinfo.md) -Auflistungs Objekte nach Wert marshallt werden. Dies impliziert, dass Komponenten, die die **IErrorInfo** -Automatisierungsschnittstelle implementieren, auch die [**IMarshal**](/windows/desktop/api/objidl/nn-objidl-imarshal) -Schnittstelle implementieren und Die Implementierung der **IMarshal** -Schnittstelle muss das Marshalling als Wert für die Komponente unterstützen.

     

-   **Verwenden Sie Transaktionen, um freigegebene Ressourcen Fehler zu verwalten.** Automatische Transaktionen können den Fehler Behandlungs Code erheblich reduzieren, den Sie bei der Verwendung von Zustands verwalteten Ressourcen-Managern schreiben müssen. Transaktionen führen jedoch nicht dazu, dass die Fehlerbehandlung vollständig durchzuführen ist. Sie müssen weiterhin Fehlercodes aus den Schnittstellen Methoden zurückgeben und diese Fehlercodes innerhalb des Aufrufers überprüfen, um unnötige Arbeit für eine nicht ordnungsgemäß erforderliche Transaktion zu vermeiden. Weitere Informationen zum Kombinieren der Fehlerbehandlung bei der Transaktionsverarbeitung finden Sie unter [beschleunigen von Transaktionen durch Benachrichtigen des Stamm Objekts](speeding-transactions-by-notifying-the-root-object.md).
-   **Fehler werden explizit ausgegeben.** Vermeiden Sie, dass Fehlerinformationen ein Objekt verlassen, es sei denn, das Objekt löst den Fehler explizit aus. Fangen Sie alle Tool generierten Fehler ab, und behandeln Sie Sie im Komponenten Code. Schließen Sie zumindest einen Standard Handler ein, um unerwartete Fehler auf konsistente Weise zu melden.
-   **Verwenden Sie den \_ Bereich für die Einrichtung von Fehler, um Schnittstellen spezifische Fehler zu melden.** Schnittstellen spezifische Fehler sollten sich in der Einrichtung im \_ Bereich von Fehlern zwischen 0x0200 und 0xFFFF befinden. Sie können einen benutzerdefinierten Fehlercode in Visual Basic als Offset von vbObjectError definieren. Verwenden Sie das \_ Makro Make HRESULT in C++, um einen schnittstellenspezifischen Fehlercode einzuführen, wie im folgenden Beispiel gezeigt:

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler Isolation und FailFast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ermitteln der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Ändern der Rückgabewerte durch com+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretieren von Fehler Codes](interpreting-error-codes.md)
</dt> <dt>

[Problembehandlung](troubleshooting.md)
</dt> </dl>

 

 
