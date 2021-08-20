---
description: Zuordnungsanbieter ermöglichen Windows WMI-Clients (Management Instrumentation), Profile und zugeordnete Klasseninstanzen aus verschiedenen Namespaces zu durchlaufen und abzurufen.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Zugreifen auf Daten im Interop-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855d3c302ca4af5381e1f0794abd643d19615dec2009740d1276698aba785d8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109644"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Zugreifen auf Daten im Interop-Namespace

Zuordnungsanbieter ermöglichen Windows WMI-Clients (Management Instrumentation), Profile und zugeordnete Klasseninstanzen aus verschiedenen Namespaces zu durchlaufen und abzurufen.

Zuordnungsanbieter und Klassen befinden sich im \\ \\ \\ Stamm-Interop-Namespace. Weitere Informationen finden Sie unter [Namespaceübergreifender Zuordnungsdurchlauf](cross-namespace-association-traversal.md) und [Schreiben eines Zuordnungsanbieters.](writing-an-association-provider-for-interop.md)

Zuordnungsanbieter machen Standardprofile verfügbar, z. B. ein Energieprofil. In den folgenden Beispielen wird das Energieprofil verwendet, um zu veranschaulichen, wie Daten über den Interop-Namespace ermittelt und darauf zugegriffen werden kann.

Windows PowerShell bietet einen einfachen Mechanismus, um die entsprechende Zuordnung zu durchlaufen, ein Geräteprofil abzurufen und eine Methode aufzurufen.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Aufzählen von Profilen im Stamm-/Interop-Namespace

Der folgende Windows PowerShell Befehl listet die von der Distributed Management Task Force[(DMTF)](https://www.dmtf.org/standards/wsman)unterstützten Profile auf einem computer Windows 7 auf:


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Abrufen von Instanzen eines bestimmten Geräteprofils

Der folgende Windows PowerShell Befehl gibt alle Instanzen eines angegebenen Profils über [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))zurück:


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Zuweisen des Energieprofils zu einer Variablen

Der folgende Windows PowerShell Befehl weist die Energieprofilinstanz einer Variablen zu:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Aufzählen der Energiesparpläne auf einem Computer

Der folgende Windows PowerShell Befehl listet die verfügbaren Energiesparpläne auf:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Aufrufen einer Methode

Der folgende Windows PowerShell Befehl ruft die [**Activate-Methode**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) für den Energiesparplan auf:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Namespaceübergreifender Zuordnungsdurchlauf](cross-namespace-association-traversal.md)
</dt> <dt>

[Schreiben eines Zuordnungsanbieters](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**Win32 \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
