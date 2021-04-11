---
description: Sie können einen Computer in für den Microsoft Update-Dienst und dann diesen Dienst bei automatische Updates registrieren.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128272"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In Microsoft Update

Sie können einen Computer in für den Microsoft Update-Dienst und dann diesen Dienst bei automatische Updates registrieren.

Das Skript Beispiel in diesem Thema zeigt Ihnen, wie Sie Windows Update-Agent (WUA) verwenden, um den Microsoft Update-Dienst bei automatische Updates zu registrieren. Alternativ kann der Benutzer Microsoft Update besuchen, um den Dienst zu registrieren.

Vergewissern Sie sich vor dem Ausführen dieses Beispiels, dass die auf dem Computer installierte Version von WUA Version 7.0.6000 oder eine höhere Version ist. Weitere Informationen zum Ermitteln der installierten Version von WUA finden Sie unter [bestimmen der aktuellen WUA](determining-the-current-version-of-wua.md)-Version.

## <a name="example"></a>Beispiel

Im folgenden Skript Beispiel wird gezeigt, wie Sie den Windows Update-Agent (WUA) verwenden, um den Microsoft Update-Dienst bei automatische Updates zu registrieren. Das Beispiel ermöglicht die verzögerte oder Offline Verarbeitung bei Bedarf.

> [!IMPORTANT]
> Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und bietet ein Beispiel dafür, wie Entwickler diese APIs zum Lösen von Problemen verwenden können. Dieses Skript ist nicht als Produktionscode gedacht, und das Skript selbst wird nicht von Microsoft unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



In früheren Versionen von WUA (mindestens eine WUA-Version von 7.0.6000) können Sie den Opt-in-Prozess vereinfachen, indem Sie eine Registrierungs Einstellung verwenden. Nachdem der Registrierungsschlüssel und die Werte konfiguriert wurden, wird der Microsoft Update Opt-in-Vorgang durchgeführt, wenn WUA das nächste Mal eine Suche durchführt. Der Opt-in-Prozess kann durch automatische Updates oder durch einen API-Aufrufer ausgelöst werden.

Der vollständige Pfad des Registrierungsschlüssels und der Werte, die für den Opt-in-Prozess festgelegt werden sollen, lauten z. b. wie folgt:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **Pdingserviceregistration** \\ **7971l918-a847-4430-9279-4a52d1efe18d**

**Clientapplicationid** = meine APP

**Registerwithau** = 1

> [!Note]
>
> Der Registrierungsschlüssel wird nur einmal beachtet, wenn WUA von einer Version, die älter ist als Version 7.0.6000, auf Version 7.0.6000 oder eine höhere Version aktualisiert wird. Beim Überschreiben vorhandener Registrierungs Werte wird ein Ermessen empfohlen, da durch das Überschreiben der Werte das Ergebnis einer früheren Dienst Registrierungs Anforderung geändert werden kann.
>
> Zum Erstellen dieses Registrierungsschlüssels sind administrative Anmelde Informationen erforderlich. Für Windows Vista muss der Aufrufer den Registrierungsschlüssel in einem erweiterten Prozess erstellen.

 

 

 



