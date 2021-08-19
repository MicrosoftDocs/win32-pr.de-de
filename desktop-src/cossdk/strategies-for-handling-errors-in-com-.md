---
description: In diesem Thema werden mehrere Fehlerbehandlungsstrategien beschrieben, die Sie beim Entwickeln von Komponenten für COM+ berücksichtigen sollten.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Strategien zum Behandeln von Fehlern in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f89736f8a81e51150e9d2480c98c6e5859d9b280fc5f7cd96662f3b1b9f3e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895700"
---
# <a name="strategies-for-handling-errors-in-com"></a>Strategien zum Behandeln von Fehlern in COM+

In diesem Thema werden mehrere Fehlerbehandlungsstrategien beschrieben, die Sie beim Entwickeln von Komponenten für COM+ berücksichtigen sollten.

-   **Gibt einen HRESULT-Wert für alle Methoden in allen Komponentenschnittstellen zurück.**  COM+ verwendet **HRESULT-Werte,** um Fehler beim Erstellen von Funktionsaufrufen oder Schnittstellenmethodeaufrufen zu melden. Ein **HRESULT gibt** an, ob eine Methode erfolgreich war oder fehlgeschlagen ist, und identifiziert die dem Fehler zugeordnete Einrichtung wie RPC, WIN32 oder ITF für schnittstellenspezifische Fehler. Darüber hinaus bieten System-APIs eine Suche von **einem HRESULT** zu einer Zeichenfolge, die den Fehlerzustand beschreibt. Die Verwendung von Methoden, die **HRESULT-Werte** zurückgeben, ist von grundlegender Bedeutung für gut geschriebene Komponenten und wichtig für den Debugprozess. Microsoft Visual Basic definiert automatisch jede Methode mit einem **HRESULT** als Rückgabe. In Microsoft Visual C++ müssen Sie explizit ein **HRESULT zurückgeben.** Weitere Informationen zu HRESULTs finden Sie unter [Struktur der COM-Fehlercodes](/windows/desktop/com/structure-of-com-error-codes).
-   **Initiieren Sie das ErrorInfo-Auflistungsobjekt mit dem, was Ihr Entwicklungstool bietet.** [**ErrorInfo-Auflistungsobjekte**](errorinfo.md) werden häufig als COM-Ausnahmen bezeichnet, da sie es einem Objekt ermöglichen, umfangreiche Fehlerinformationen an den Aufrufer zu übergeben (oder zu auslösen), auch über Apartmentgrenzen hinweg. Der Wert dieses generischen Fehlerobjekts ist, dass es ein HRESULT ergänzt und den Typ der Fehlerinformationen erweitert, die Sie an einen Aufrufer zurückgeben können. Jedes **ErrorInfo-Auflistungsobjekt** gibt eine kontextbezogene Beschreibung, die Fehlerquelle und den Schnittstellenbezeichner der Methode zurück, die den Fehler verursacht hat. Sie können auch Zeiger auf einen Eintrag in einer Hilfedatei enthalten. Automation bietet drei Schnittstellen zum Verwalten des Fehlerobjekts. Ihre Komponente muss die **ISupportErrorInfo Automation-Schnittstelle** implementieren, um deren Unterstützung für die **ErrorInfo-Sammlung anklicken zu** können. Wenn ein Fehler auftritt, verwendet die Komponente die **ICreateErrorInfo** Automation-Schnittstelle, um ein Fehlerobjekt zu initialisieren. Nachdem der Aufrufer das HRESULT überprüft und ermittelt hat, dass der Methodenaufruf fehlgeschlagen ist, fragt er das -Objekt ab, um festzustellen, ob es die **ErrorInfo-Auflistung** unterstützt. In diesem Beispiel verwendet der Aufrufer die **IErrorInfo-Automatisierungsschnittstelle,** um die Fehlerinformationen abzurufen. Visual Basic haben einfachen Zugriff auf  das ErrorInfo-Auflistungsobjekt, das über das Err-Objekt verfügbar gemacht wird. Sie können Fehler mit der Err Raise-Funktion beheben und Fehler mit der **On Error-Anweisung** abfangen. Die Visual Basic-Laufzeitebene übernimmt die Zuordnung für Sie. Wenn Sie die com Visual C++compilerunterstützung verwenden, können Sie die com raise error-Klasse verwenden, um einen Fehler zu melden, und die com-Fehlerklasse, um \_ \_ \_ \_ \_ Fehlerinformationen abzurufen. COM+ gibt herkömmliche C++-Ausnahmen nicht als erweiterte **IErrorInfo-Informationen** weiter. Weitere Informationen zum **ErrorInfo-Auflistungsobjekt** finden Sie im Automation-Handbuch unter "Fehlerbehandlung".
    > [!Note]  
    > COM erfordert, [](errorinfo.md) dass alle ErrorInfo-Auflistungsobjekte nach Wert gemarshallt werden, was bedeutet, dass Komponenten, die die **IErrorInfo-Automatisierungsschnittstelle** implementieren, auch die [**IMarshal-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-imarshal) implementieren und unterstützen müssen. Die **IMarshal-Schnittstellenimplementierung** muss marshallen als Wert für die Komponente unterstützen.

     

-   **Verwenden Sie Transaktionen, um Fehler bei freigegebenen Ressourcen zu verwalten.** Automatische Transaktionen können die Menge an Fehlerbehandlungscode, den Sie schreiben müssen, bei Verwendung von zustandsver verwalteten Ressourcen-Managern erheblich reduzieren. Transaktionen entfällt jedoch nicht ganz auf die Notwendigkeit der Fehlerbehandlung. Sie müssen weiterhin Fehlercodes von Ihren Schnittstellenmethoden zurückgeben und diese Fehlercodes innerhalb des Aufrufers überprüfen, um unnötige Arbeit für eine nicht zu verhindernde Transaktion zu vermeiden. Weitere Informationen zum Kombinieren der Fehlerbehandlung mit der Transaktionsverarbeitung finden Sie unter Beschleunigen von [Transaktionen durch Benachrichtigen des Stammobjekts](speeding-transactions-by-notifying-the-root-object.md).
-   **Explizites Auftreten von Fehlern.** Vermeiden Sie, dass Fehlerinformationen ein Objekt verlassen, es sei denn, das Objekt löst den Fehler explizit aus. Fangen Sie alle vom Tool generierten Fehler ab, und behandeln Sie sie in Ihrem Komponentencode. Schließen Sie zumindest einen Standardhandler ein, um unerwartete Fehler konsistent zu melden.
-   **Verwenden Sie den FACILITY \_ ITF-Fehlerbereich, um schnittstellenspezifische Fehler zu melden.** Schnittstellenspezifische Fehler sollten im FACILITY ITF-Fehlerbereich zwischen 0x0200 \_ und 0xFFFF. Sie können einen benutzerdefinierten Fehlercode in Visual Basic offset von vbObjectError definieren. Verwenden Sie das MAKE \_ HRESULT-Makro in C++, um einen schnittstellenspezifischen Fehlercode einzuführen, wie im folgenden Beispiel gezeigt:

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerisolation und Failfast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Suchen der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Ändern von Rückgabewerten durch COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretieren von Fehlercodes](interpreting-error-codes.md)
</dt> <dt>

[Problembehandlung](troubleshooting.md)
</dt> </dl>

 

 
