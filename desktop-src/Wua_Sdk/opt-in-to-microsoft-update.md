---
description: Sie können einen Computer für den Microsoft Update-Dienst anmelden und diesen Dienst dann bei Automatische Updates.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In sie Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d034f0b224d8170a52ce359589693c601cb9598d716e9663493e8ac99edf2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994278"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In sie Microsoft Update

Sie können einen Computer für den Microsoft Update-Dienst anmelden und diesen Dienst dann bei Automatische Updates.

Das Skriptbeispiel in diesem Thema zeigt, wie Sie den Windows Update-Agent (WUA) verwenden, um den Microsoft Update-Dienst bei Automatische Updates. Alternativ kann der Benutzer zum Registrieren des Diensts Microsoft Update.

Vergewissern Sie sich vor dem Ausführen dieses Beispiels, dass die auf dem Computer installierte WUA-Version Version 7.0.6000 oder höher ist. Weitere Informationen zum Bestimmen der installierten WUA-Version finden Sie unter [Determining the Current Version of WUA](determining-the-current-version-of-wua.md)( Bestimmen der aktuellen Version von WUA ).

## <a name="example"></a>Beispiel

Das folgende Skriptbeispiel zeigt, wie Sie den Windows Update-Agent (WUA) verwenden, um den Microsoft Update-Dienst bei Automatische Updates. Das Beispiel ermöglicht bei Bedarf eine verzögerte oder Offlineverarbeitung.

> [!IMPORTANT]
> Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und ein Beispiel dafür bereitstellen, wie Entwickler diese APIs verwenden können, um Probleme zu lösen. Dieses Skript ist nicht als Produktionscode gedacht, und das Skript selbst wird von Microsoft nicht unterstützt (obwohl die zugrunde liegenden Windows-Agent-APIs unterstützt werden).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



In früheren Versionen von WUA (wua-Mindestversion 7.0.6000) können Sie den Opt-In-Prozess vereinfachen, indem Sie eine Registrierungseinstellung verwenden. Nachdem der Registrierungsschlüssel und die Werte konfiguriert wurden, Microsoft Update der Registrierungsprozess bei der nächsten WuA-Suche. Der Opt-In-Prozess kann durch einen Automatische Updates oder durch einen API-Aufrufer ausgelöst werden.

Der vollständige Pfad des Registrierungsschlüssels und der Werte, die für den Opt-In-Prozess festgelegt werden sollen, lautet beispielsweise wie folgt:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsUpdate** \\ **PendingServiceRegistration** \\ **7971f918-a847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = Meine App

**RegisterWithAU** = 1

> [!Note]
>
> Der Registrierungsschlüssel wird nur einmal beachtet, wenn WUA von einer früheren Version als Version 7.0.6000 auf Version 7.0.6000 oder auf eine neuere Version aktualisiert wird. Es wird empfohlen, beim Überschreiben vorhandener Registrierungswerte einen ermessenswerten Wert zu haben, da das Überschreiben der Werte das Ergebnis einer früheren Dienstregistrierungsanforderung ändern kann.
>
> Zum Erstellen dieses Registrierungsschlüssels sind Administratoranmeldeinformationen erforderlich. Für Windows Vista muss der Aufrufer den Registrierungsschlüssel in einem Prozess mit erhöhten Rechten erstellen.

 

 

 



