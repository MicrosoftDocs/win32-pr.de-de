---
description: Mithilfe von Zuordnungs Anbietern können Windows-Verwaltungsinstrumentation (WMI)-Clients Profile und zugehörige Klassen Instanzen aus unterschiedlichen Namespaces durchlaufen und abrufen.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Zugreifen auf Daten im Interop-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960618"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Zugreifen auf Daten im Interop-Namespace

Mithilfe von Zuordnungs Anbietern können Windows-Verwaltungsinstrumentation (WMI)-Clients Profile und zugehörige Klassen Instanzen aus unterschiedlichen Namespaces durchlaufen und abrufen.

Zuordnungs Anbieter und-Klassen befinden sich im \\ \\ \\ Namespace "root Interop". Weitere Informationen finden Sie unter [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) und [Writing a Association Provider](writing-an-association-provider-for-interop.md).

Zuordnungs Anbieter machen Standardprofile wie z. b. ein Power Profile verfügbar. In den folgenden Beispielen wird das Power Profile verwendet, um zu veranschaulichen, wie Sie Daten mithilfe des Interop-Namespace ermitteln und darauf zugreifen können.

Windows PowerShell bietet einen einfachen Mechanismus zum Durchlaufen der entsprechenden Zuordnung, zum Abrufen eines Geräte Profils und zum Aufrufen einer Methode.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Auflisten von Profilen im Root/Interop-Namespace

Mit dem folgenden Windows PowerShell-Befehl werden die von der[DMTF](https://www.dmtf.org/standards/wsman)(verteilte Management Task Force) unterstützten Profile auf einem Windows 7-Computer aufgelistet:


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Abrufen von Instanzen eines bestimmten Geräte Profils

Mit dem folgenden Windows PowerShell-Befehl werden alle Instanzen eines angegebenen Profils über [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))zurückgegeben:


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Zuweisen des Power Profile zu einer Variablen

Der folgende Windows PowerShell-Befehl weist die Power profile-Instanz einer Variablen zu:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Auflisten von Energie Sparplänen auf einem Computer

Der folgende Windows PowerShell-Befehl listet die verfügbaren Energieprofil Pläne auf:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Aufrufen einer Methode

Der folgende Windows PowerShell-Befehl ruft die [**Aktivierungs**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) Methode für den Energie Sparplan auf:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Cross-Namespace Association Traversal](cross-namespace-association-traversal.md)
</dt> <dt>

[Schreiben eines Zuordnungs Anbieters](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**Win32- \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
