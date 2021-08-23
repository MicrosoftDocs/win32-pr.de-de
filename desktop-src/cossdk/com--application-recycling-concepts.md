---
description: Die Wiederverwendung von Anwendungen kann die Gesamtstabilität Ihrer COM+-Anwendungen erheblich erhöhen, indem eine schnelle Lösung für bekannte Probleme und der Schutz vor unerwarteten Problemen angeboten wird.
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: COM+-Konzepte für die Wiederverwendung von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a635487427fce3f17203f11426261996348a5e4057ab8bceebcae552d51bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129262"
---
# <a name="com-application-recycling-concepts"></a>COM+-Konzepte für die Wiederverwendung von Anwendungen

Die Wiederverwendung von Anwendungen kann die Gesamtstabilität Ihrer COM+-Anwendungen erheblich erhöhen, indem eine schnelle Lösung für bekannte Probleme und der Schutz vor unerwarteten Problemen angeboten wird. Beispielsweise kann die Anwendungsleistung im Laufe der Zeit aufgrund von Problemen wie Speicherverlusten, nicht skalierbarer Ressourcennutzung und Prozessfehlern beeinträchtigt werden. COM+ bietet die Wiederverwendung von Anwendungen als Lösung für diese Probleme. Sie können die Wiederverwendung von Anwendungen verwenden, um einen Prozess automatisch herunter- und neu zu starten, wodurch ein fehlerhafter Prozess erneut initialisiert und der von ihm verwendete Arbeitsspeicher neu zugewiesen wird.

Bei der Anwendungswiederverwendung wird ein Duplikat des Dllhost-Prozesses erstellt, der einer Anwendung zugeordnet ist. Dieser doppelte Dllhost-Prozess bedient alle zukünftigen Objektanforderungen, wodurch der alte Dllhost die Verarbeitung der verbleibenden Objektanforderungen beendet. Der alte Dllhost-Prozess wird heruntergefahren, wenn er die Freigabe aller externen Verweise auf Objekte im Prozess erkennt oder wenn der Time out-Wert für den Ablauf erreicht wird. Durch dieses Verhalten wird durch die Wiederverwendung von Anwendungen sichergestellt, dass es bei einer Clientanwendung nicht zu einer Dienstunterbrechung kommt.

> [!Note]  
> Sie können keine COM+-Anwendung wiederverwerten, die für die Ausführung als Windows wurde. Darüber hinaus verfügen Bibliotheksanwendungen über die Wiederverwendungs- und Poolingeigenschaften ihres Hostprozesses.

 

Sie können die Wiederverwendung von Anwendungen mithilfe des Komponentendienste-Verwaltungstools oder programmgesteuert über das COM+-Verwaltungs-SDK konfigurieren. Sie können Prozesse basierend auf mehreren Kriterien wiederverwerten, die durch die folgenden Eigenschaften eines [**COMAdminCatalogObject-Objekts**](comadmincatalogobject.md) in der [**Anwendungssammlung bestimmt**](applications.md) werden:

-   **RecycleLifetimeLimit.** Die maximale Anzahl von Minuten, die ein Prozess ausgeführt werden kann, bevor er wiederverwendet wird. Der gültige Bereich beträgt 0 bis 30.240 Minuten (21 Tage). Die Standardanzahl von Minuten ist 0. Dies bedeutet, dass der Prozess nicht wiederverwertet wird, wenn ein Lebensdauerlimit erreicht wird.
-   **RecycleMemoryLimit.** Die maximale Prozessspeicherauslastung (in Kilobytes), bevor der Prozess wiederverwertet wird. Wenn die Arbeitsspeicherauslastung des Prozesses länger als eine Minute die angegebene Anzahl überschreitet, wird der Prozess wiederverwendet. Der gültige Bereich liegt zwischen 0 und 1.048.576 KB. Die Standardmenge der Arbeitsspeicherauslastung beträgt 0 KB, was darauf hinweist, dass der Prozess nicht wiederverwertet wird, wenn ein Arbeitsspeicherlimit erreicht wird.
-   **RecycleCallLimit.** Die maximale Anzahl von Aufrufen, die Anwendungsobjekte akzeptieren können, bevor der Prozess wieder verwendet wird. Der gültige Bereich liegt zwischen 0 und 1.048.576 Aufrufen. Die Standardanzahl der Aufrufe ist 0. Dies bedeutet, dass der Prozess nicht vom Erreichen eines Aufruflimits wiederverwendet wird.
-   **RecycleActivationLimit.** Die maximale Anzahl von Anwendungsobjektaktivierungen, die vor der Wiederverwendung des Prozesses akzeptiert werden. Der gültige Bereich liegt zwischen 0 und 1.048.576 Aktivierungen. Die Standardanzahl der Aktivierungen ist 0 ( 0). Dies bedeutet, dass der Prozess nicht vom Erreichen eines Aktivierungslimits wiederverwendet wird.

Darüber hinaus wird die RecycleExpirationTimeout-Eigenschaft des [**COMAdminCatalogObject-Objekts**](comadmincatalogobject.md) verwendet, um das Herunterfahren eines wiederverwendeten Prozesses zu erzwingen. Gibt an, wie viele Minuten auf die Freigabe aller externen Verweise auf Objekte im wiederverwendeten Prozess gewartet werden soll, bevor der Prozess beendet wird. Der gültige Bereich beträgt 1 bis 1440 Minuten (24 Stunden), und das Standardablauf-Time out beträgt 15 Minuten. Dieser Wert wird nur verwendet, wenn bereits bestimmt wurde, dass ein Prozess basierend auf den anderen Kriterien wiederverwendet wird.

Sie können mehrere Kriterien für die Wiederverwendung einer Anwendung auswählen. COM+ verwendet die Anwendung wieder, nachdem der erste Kriteriensatz erfüllt wurde. Sie können den Wert für ablaufendes Time out festlegen, um zu bestimmen, wie lange ein alter Dllhost-Prozess verbleibende Dienstanforderungen abschließen kann, bevor er zum Herunterfahren gesperrt wird.

Die [**ApplicationInstances-Auflistung**](applicationinstances.md) stellt die HasRecycled-Eigenschaft bereit, die eine Möglichkeit bietet, zu bestimmen, ob die Anwendung jemals wiederverwendet wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Anwendungswiederverwendungsaufgaben](com--application-recycling-tasks.md)
</dt> <dt>

[**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



