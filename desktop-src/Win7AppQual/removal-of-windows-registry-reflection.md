---
description: Entfernen der Windows Registry Reflection
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Entfernen der Windows Registry Reflection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9fcd31686754f9bf2d92994bec4a53b39edaf5d94b34f464e1dfdbf1179c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328979"
---
# <a name="removal-of-windows-registry-reflection"></a>Entfernen der Windows Registry Reflection

## <a name="platform"></a>Plattform

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Niedrig  





## <a name="description"></a>Beschreibung

Der Registrierungslektionsprozess kopiert Registrierungsschlüssel und -werte zwischen zwei Registrierungssichten, um sie synchron zu halten. In früheren 64-Bit-Installationen von Windows spiegelte der Prozess eine Teilmenge der umgeleiteten Registrierungsschlüssel zwischen den 32-Bit- und 64-Bit-Ansichten wider. Die Implementierung dieses führte jedoch zu einigen Inkonsistenzen im Zustand der Registrierung. (Weitere Informationen zur Reflektion von Registrierungen finden Sie im entsprechenden MSDN-Artikel im Abschnitt *Links zu anderen* Ressourcen weiter unten.)

Ab Windows 7 haben wir die Registrierungslektion vollständig entfernt und die Schlüssel zusammengeführt, die früher widergespiegelt wurden:

-   HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ COM3
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ EventSystem
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Ole
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc
-   HKEY \_ \\ \* \\ \\ USERS-Softwareklassen
-   HKEY \_ \\ \* \_ USERS-Klassen

Effektiv bietet dies das gleiche Reflektionsverhalten, da Änderungen an diesen Schlüsseln sofort sowohl für 32-Bit- als auch für 64-Bit-Anwendungen verfügbar sind.

Die Schlüssel, die bedingt widergespiegelt wurden, bleiben aufgeteilt:

-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ CLSID
-   HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ Interface
-   HKEY \_ \\ \* \\ USERS-Softwareklassen \\ \\ CLSID
-   HKEY \_ USERS \\ \* \\ Software \\ Classes \\ Interface
-   HKEY \_ \\ \* \_ USERS-Klassen \\ CLSID
-   HKEY \_ \\ \* \_ \\ USERS-Klassenschnittstelle

Sie werden verwendet, um die Daten zu behalten, die nicht von 32-Bit- und 64-Bit-Anwendungen gemeinsam genutzt werden sollen.

## <a name="manifestation"></a>Manifestation

CLSID- und Schnittstellenschlüssel aus der obigen Liste werden nicht mehr widergespiegelt, während sie noch umgeleitet werden. Obwohl dies in den meisten Fällen das gewünschte Verhalten ist, ist es möglich, dass Anwendungen von ihrem reflektierten Verhalten in Vista abhängig sind.

Die Funktionen, mit denen Anwendungen reflektion steuern können (RegDisableReflectionKey und RegEnableReflectionKey), sind in Windows 7 keine Funktionen.

## <a name="mitigation-of-impact"></a>Entschärfung der Auswirkungen

COM ist der Hauptverbraucher der Registrierungslektion. COM und andere Verbraucher wurden aktualisiert, um diese Änderung zu nutzen. Diese Änderung wirkt sich nicht auf Anwendungen aus, die COM-Standard-APIs verwenden.

## <a name="solution"></a>Lösung

Wenden Sie eine der folgenden Optionen an, wenn Sie sich auf die Reflektion der Registrierung verlassen, um 32-Bit- und 64-Bit-Ansichten zu synchronisieren:

-   Explizites Erstellen von Schlüsseln in beiden Ansichten während der Installation
-   Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel
-   Überprüfen beider Ansichten der Registrierung beim Abfragen eines reflektierten Schlüssels

    **Hinweis:** KEY \_ WOW64 \_ 32KEY- und KEY \_ WOW64 \_ 64KEY-Flags können nicht kombiniert werden

Wenden Sie eine der folgenden Optionen an, wenn Sie regDisableReflectionKey-Funktionen verwenden, um die Reflektion der Registrierung zu deaktivieren:

-   Explizites Erstellen von Schlüsseln in beiden Ansichten während der Installation
-   Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel
-   Verwenden Sie plattformspezifische Unterschlüssel (wie x86, amd64 und ia64), um bitspezifische Daten zu trennen.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Artikel zur Registrierungslektion](../winprog64/registry-reflection.md)
-   [Liste der umgeleiteten Schlüssel im Artikel "Registrierungsumleitung"](../winprog64/registry-redirector.md)
-   [Bewährte Methoden für Wow64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.

 

 

 
