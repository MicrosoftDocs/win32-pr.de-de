---
description: Durch die Wiederverwendung von Anwendungen können Sie die Gesamtstabilität ihrer com+-Anwendungen beträchtlich erhöhen, indem Sie eine schnelle Lösung für bekannte Probleme bieten und Schutz vor unerwarteten Problemen bieten.
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: Konzepte der com+-Anwendungs Wiederverwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab37376ff3bc6d03f454f63822641ed69fad0b47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393018"
---
# <a name="com-application-recycling-concepts"></a>Konzepte der com+-Anwendungs Wiederverwendung

Durch die Wiederverwendung von Anwendungen können Sie die Gesamtstabilität ihrer com+-Anwendungen beträchtlich erhöhen, indem Sie eine schnelle Lösung für bekannte Probleme bieten und Schutz vor unerwarteten Problemen bieten. Beispielsweise kann die Anwendungsleistung im Lauf der Zeit aufgrund von Problemen wie Speicherlecks, nicht skalierbarer Ressourcenverwendung und Prozessfehlern beeinträchtigt werden. Com+ bietet Anwendungs Wiederverwendung als Lösung für diese Probleme. Mithilfe der Anwendungs Wiederverwendung können Sie einen Prozess automatisch Herunterfahren und neu starten. auf diese Weise können Sie einen fehlerhaften Prozess erneut initialisieren und den verwendeten Speicher neu zuordnen.

Die Anwendungs Wiederverwendung funktioniert, indem ein Duplikat des dllhost-Prozesses erstellt wird, der einer Anwendung zugeordnet ist. Mit diesem doppelten dllhost-Prozess werden alle zukünftigen Objekt Anforderungen verarbeitet, sodass der alte dllhost die Wartung der restlichen Objekt Anforderungen verlässt. Der alte dllhost-Prozess wird heruntergefahren, wenn er das Release aller externen Verweise auf Objekte im Prozess erkennt oder wenn der Ablauf Timeout Wert erreicht wird. Durch dieses Verhalten stellt die Anwendungs Wiederverwendung sicher, dass bei einer Client Anwendung keine Dienst Unterbrechung auftritt.

> [!Note]  
> Eine COM+-Anwendung, die für die Verwendung als Windows-Dienst konfiguriert wurde, kann nicht wieder verwendet werden. Außerdem verfügen Bibliotheksanwendungen über die Eigenschaften zum wieder verwenden und zum Pooling Ihres Host Prozesses.

 

Mithilfe des Verwaltungs Tools Komponenten Dienste oder Programm gesteuert über das com+-Verwaltungs-SDK können Sie die Anwendungs Wiederverwendung administrativ konfigurieren. Sie können Prozesse auf der Grundlage verschiedener Kriterien wieder verwenden, die durch die folgenden Eigenschaften eines [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekts in der [**Anwendungs**](applications.md) Auflistung bestimmt werden:

-   **"Recyclelifetimelimit".** Die maximale Anzahl von Minuten, die ein Prozess ausgeführt werden kann, bevor er wieder verwendet wird. Der gültige Bereich liegt zwischen 0 und 30.240 Minuten (21 Tage). Die Standard Anzahl von Minuten ist 0 (null). Dies bedeutet, dass der Prozess nicht wieder verwendet werden kann, um eine Lebensdauer zu erreichen.
-   **Recyclememorylimit.** Die maximale Menge an Prozess Speicherauslastung (in Kilobyte), bevor der Prozess wieder verwendet wird. Wenn die Prozess Speicherauslastung die angegebene Anzahl länger als eine Minute überschreitet, wird der Prozess wieder verwendet. Der gültige Bereich liegt zwischen 0 und 1.048.576 KB. Der Standardwert für die Speicherauslastung beträgt 0 KB. Dies bedeutet, dass der Prozess das Erreichen eines Arbeitsspeicher Limits nicht wieder verwendet.
-   **"RecycleCallLimit".** Die maximale Anzahl von aufrufen, die von Anwendungs Objekten angenommen werden können, bevor der Prozess wieder verwendet wird. Der gültige Bereich liegt zwischen 0 und 1.048.576 aufrufen. Die Standard Anzahl von Aufrufen ist 0 (null), was darauf hinweist, dass der Prozess das Erreichen eines Aufruf Limits nicht wieder verwendet.
-   **Recycleactivationlimit.** Die maximale Anzahl von Anwendungs Objekt Aktivierungen, die vor der Wiederverwendung des Prozesses akzeptiert werden sollen. Der gültige Bereich liegt zwischen 0 und 1.048.576 Aktivierungen. Die Standard Anzahl von Aktivierungen ist 0 (null), was darauf hinweist, dass der Prozess das Erreichen eines Aktivierungs Limits nicht wieder verwendet.

Außerdem wird die Eigenschaft "recycleexpirationtimeout" des Objekts " [**COMAdminCatalogObject**](comadmincatalogobject.md) " verwendet, um das Herunterfahren eines wiederverwendeten Prozesses zu erzwingen. Gibt die Anzahl von Minuten an, die auf das Release aller externen Verweise auf Objekte im wiederverwendeten Prozess gewartet werden soll, bevor der Prozess beendet wird. Der gültige Bereich liegt zwischen 1 und 1440 Minuten (24 Stunden), und das Standard Ablauf Timeout beträgt 15 Minuten. Dieser Wert wird nur verwendet, wenn bereits festgestellt wurde, dass ein Prozess basierend auf den anderen Kriterien wieder verwendet wird.

Sie können mehr als ein Kriterium für die Wiederverwendung einer Anwendung auswählen. Com+ wieder verwendet die Anwendung, nachdem der erste Satz Kriterien erfüllt wurde. Sie können den Timeout Wert für den Ablauf festlegen, um zu bestimmen, wie lange ein Alter dllhost-Prozess verbleibende Dienst Anforderungen abschließen kann, bevor das Herunterfahren erzwungen wird.

Die [**ApplicationInstance**](applicationinstances.md) -Auflistung stellt die hasrecycelt-Eigenschaft bereit, die eine Möglichkeit bietet, zu bestimmen, ob die Anwendung jemals wieder verwendet wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Anwendungs Wiederverwendungs Tasks](com--application-recycling-tasks.md)
</dt> <dt>

[**Recycleersatz**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



