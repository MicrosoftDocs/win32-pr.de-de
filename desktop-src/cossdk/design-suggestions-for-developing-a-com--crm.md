---
description: Entwurfsvorschläge für die Entwicklung eines com+ CRM
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Entwurfsvorschläge für die Entwicklung eines com+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dcdb59f0ea23fb6879300d0bacec7df12970d81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214144"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Entwurfsvorschläge für die Entwicklung eines com+ CRM

Die folgenden Schritte sind für die Entwicklung eines com+-CRM empfehlenswert:

1.  Legen Sie vor dem Starten der Entwicklung den Transaktions Timeout auf NULL (mithilfe des Verwaltungs Programms Komponenten Dienste) fest. Legen Sie das VTRACE1-Registrierungsflag fest (siehe [com+ CRM-Registrierungs Einstellungen](com--crm-registry-settings.md)), um CRM-Warn-und Fehlermeldungen in der Debugablaufverfolgung anzuzeigen
2.  Bestimmen Sie, welche Gruppe von Schnittstellen Sie verwenden möchten, strukturiert (Varianten) oder nicht strukturiert ist. (Siehe [com+ CRM-Schnittstellen](com--crm-interfaces.md).) Dies hängt von der Sprache ab, die Sie für die Entwicklung Ihres CRM verwenden – z. b. Microsoft Visual C++ oder Microsoft Visual Basic.
3.  Entwickeln Sie zuerst den CRM-Worker. Bestimmen Sie die Informationen, die in den Protokolldaten Sätzen benötigt werden. Definieren Sie die Typen von erforderlichen Protokolldaten Sätzen und deren Format.
4.  Ein Debug CRM Kompensator wird als Teil der CRM-Beispiele (im Windows SDK) bereitgestellt. Dies kann vorübergehend beim Debuggen des CRM-Workers anstelle des echten CRM-kompenators verwendet werden.
5.  Wenn der CRM-Worker ordnungsgemäß funktioniert, entwickeln Sie den Real CRM-kompenatordienst, und ersetzen Sie den Debug CRM Kompensator durch den Real CRM Kompensator.
6.  Es kann wünschenswert sein, den Wiederherstellungs Fall anfänglich nicht zu testen. Wenn dies der Fall ist, löschen Sie die CRM-Protokolldatei für die CRM-Serveranwendung, bevor Sie diese CRM-Serveranwendung starten.

## <a name="considerations"></a>Überlegungen

1.  **Schreiben Sie weiter.** Die CRM-workerkomponente muss im Voraus schreiben. Das heißt, es muss einen Protokolldaten Satz schreiben, der angibt, dass eine Aktion ausgeführt wird, bevor diese Aktion tatsächlich durchgeführt wird. Außerdem muss dieser Protokolldaten Satz nach dem Schreibvorgang und vor der Ausführung der Aktion auf den Datenträger erzwungen werden.
2.  **Isolation.** Das CRM erzwingt keine Isolation. Der CRM-Entwurf muss die Isolation zwischen mehreren Clients auf separaten Transaktionen bereitstellen und muss auch den Fall vor der Wiederherstellung in Erwägung gezogen werden.
3.  **Wiederherstellung wird durchgeführt.** Der CRM-Worker muss den Fehlercode "Wiederherstellung in Bearbeitung" verarbeiten. Weitere Informationen zu diesem Fehlercode finden Sie [unter Problembehandlung beim com+-CRM](troubleshooting-the-com--crm.md) .
4.  **Fehlerbehandlung.** Der CRM-Worker muss mit dem Fall zurechtkommen, dass die Transaktion früher als erwartet abgebrochen wurde. Weitere Informationen finden Sie [im Abschnitt Fehlerbehandlung in com+ CRM](error-handling-in-the-com--crm.md).
5.  **Wiederherstellungszeit.** Der CRM-kompenerer sollte so konzipiert werden, dass er die Wiederherstellung schnell durchführt, damit neue Aufgaben für diese CRM-Serveranwendung nicht gewartet werden müssen.
6.  **Idempotenz.** Es ist möglich, dass ein CRM-Kompensator den gleichen Protokolldaten Satz möglicherweise erneut empfängt, um eine Aktion rückgängig zu machen oder wiederholen, die bereits rückgängig gemacht oder wiederholt wurde. Aktionen, die der CRM-kompenerer ausführen kann, müssen idempotent sein, was häufig bedeutet, dass die von diesen Aktionen zurückgegebenen Fehlercodes ignoriert werden sollten.
7.  **Initiierung der Wiederherstellung.** Die Wiederherstellung einer CRM-Serveranwendung wird ausgeführt, wenn diese CRM-Serveranwendung gestartet wird. Eine CRM-Serveranwendung wird jedoch nicht automatisch gestartet. Der Anwendungsentwickler sollte in Erwägung gezogen werden, wie Start-und Wiederherstellungs Vorgang initiiert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



