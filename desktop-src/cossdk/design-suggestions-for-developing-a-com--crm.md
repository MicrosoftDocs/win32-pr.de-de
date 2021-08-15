---
description: Entwurfsvorschläge für die Entwicklung eines COM+-CRM
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Entwurfsvorschläge für die Entwicklung eines COM+-CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a286b2aa75b266a41b249b29203b16f0441e6276a9de03a25efc622ac2bd3fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128752"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Entwurfsvorschläge für die Entwicklung eines COM+-CRM

Im Folgenden werden schritte für die Entwicklung eines COM+-CRM-Systems vorgeschlagen:

1.  Legen Sie vor Beginn der Entwicklung das Transaktionstime out auf 0 (mithilfe des Verwaltungstools Komponentendienste) fest. Legen Sie das VTRACE1-Registrierungsflag fest (siehe [COM+ CRM-Registrierung Einstellungen](com--crm-registry-settings.md)), um CRM-Warnungen und -Fehlermeldungen in der Debugablaufverfolgung anzuzeigen.
2.  Bestimmen Sie, welche Schnittstellen Sie verwenden müssen, strukturiert (Varianten) oder nicht strukturiert. (Siehe [COM+ CRM-Schnittstellen](com--crm-interfaces.md).) Dies hängt von der Sprache ab, die Sie zum Entwickeln Ihres CRM verwenden, z. B. Microsoft Visual C++ oder Microsoft Visual Basic.
3.  Entwickeln Sie zuerst den CRM-Worker. Bestimmen Sie die Informationen, die in den Protokolldatensätzen erforderlich sind. Definieren Sie die Erforderlichen Typen von Protokolldatensätzen und deren Format.
4.  Ein CRM-Kompensator zum Debuggen wird als Teil der CRM-Beispiele (im Windows SDK) bereitgestellt. Dies kann beim Debuggen des CRM-Workers anstelle des tatsächlichen CRM-Kompensators vorübergehend verwendet werden.
5.  Wenn der CRM-Worker ordnungsgemäß arbeitet, entwickeln Sie den echten CRM-Kompensator und ersetzen den CRM-Debugkompensator durch den echten CRM-Kompensator.
6.  Es kann wünschenswert sein, den Wiederherstellungsfall zunächst nicht zu testen. Löschen Sie in diesem Falle jedes Mal die CRM-Protokolldatei für die CRM-Serveranwendung, bevor Sie diese CRM-Serveranwendung starten.

## <a name="considerations"></a>Überlegungen

1.  **Schreiben Sie im Voraus.** Die CRM-Workerkomponente muss voranschreiben. Das heißt, er muss einen Protokolldatensatz schreiben, der angibt, dass eine Aktion ausgeführt wird, bevor diese Aktion tatsächlich ausgeführt wird. Darüber hinaus muss dieser Protokolldatensatz nach dem Schreibvorgang und vor dem Durchführen der Aktion auf den Datenträger erzwungen werden.
2.  **Isolation.** Das CRM erzwingt keine Isolation. Der CRM-Entwurf muss eine Isolation zwischen mehreren Clients bei separaten Transaktionen bereitstellen und den Fall vor der Wiederherstellung berücksichtigen.
3.  **Wiederherstellung wird ausgeführt.** Der CRM-Worker muss den Fehlercode "Wiederherstellung wird ausgeführt" behandeln. Weitere Informationen zu diesem Fehlercode finden Sie unter Problembehandlung für [COM+ CRM.](troubleshooting-the-com--crm.md)
4.  **Fehlerbehandlung.** Der CRM-Worker muss den Fall bewältigen, in dem die Transaktion früher als erwartet abgebrochen wird. Weitere Informationen finden Sie im Abschnitt [Fehlerbehandlung in COM+ CRM.](error-handling-in-the-com--crm.md)
5.  **Wiederherstellungszeit.** Der CRM-Kompensator sollte so konzipiert sein, dass die Wiederherstellung schnell durchgeführt wird, sodass neue Aufgaben für diese CRM-Serveranwendung nicht warten müssen.
6.  **Idempotenz.** Es ist möglich, dass ein CRM-Kompensator denselben Protokolldatensatz erneut erhält, um eine Aktion rückgängig zu machen oder zu wiederholen, die bereits rückgängig gemacht oder wiederholt wurde. Aktionen, die der CRM-Kompensator ausführen kann, müssen idempotent sein. Dies bedeutet häufig, dass die von diesen Aktionen zurückgegebenen Fehlercodes ignoriert werden sollten.
7.  **Initiierung der Wiederherstellung.** Die Wiederherstellung einer CRM-Serveranwendung wird ausgeführt, wenn diese CRM-Serveranwendung gestartet wird. Es gibt jedoch keinen automatischen Start einer CRM-Serveranwendung. Der Anwendungsentwickler sollte überlegen, wie sowohl der Start als auch die Wiederherstellung initiiert werden sollen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Concepts](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



