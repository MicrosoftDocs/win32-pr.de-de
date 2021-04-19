---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Entfernen der Windows-Registrierungs Reflektion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364215"
---
# <a name="removal-of-windows-registry-reflection"></a>Entfernen der Windows-Registrierungs Reflektion

## <a name="platform"></a>Plattform

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Der Registrierungs Reflektionsprozess kopiert Registrierungsschlüssel und-Werte zwischen zwei Registrierungs Sichten, um sie synchron zu halten. In früheren 64-Bit-Installationen von Windows hat der Prozess eine Teilmenge der umgeleiteten Registrierungsschlüssel zwischen den 32-Bit-und 64-Bit-Sichten reflektiert. Die Implementierung dieser Ursache hat jedoch einige Inkonsistenzen im Zustand der Registrierung verursacht. (Ausführliche Informationen zur Registrierungs Reflektion finden Sie im entsprechenden MSDN-Artikel im Abschnitt *Links zu anderen Ressourcen* weiter unten.)

Ab Windows 7 haben wir die Registrierungs Reflektion vollständig entfernt und die Schlüssel zusammengeführt, die für die Wiederverwendung verwendet wurden:

-   HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer
-   HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ COM3
-   HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ EventSystem
-   HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE
-   HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ RPC
-   \_ \\ \* \\ Software \\ Klassen für HKEY-Benutzer
-   HKEY- \_ Benutzer \\ \* \_ Klassen

Dadurch wird das gleiche Reflektionsverhalten bereitgestellt, da Änderungen an diesen Schlüsseln sofort für 32-Bit-und 64-Bit-Anwendungen verfügbar sind.

Die Schlüssel, die bedingt reflektiert wurden, bleiben getrennt:

-   HKEY \_ - \_ \\ Software \\ Klassen- \\ CLSID für lokale Computer
-   Schnittstelle für HKEY- \_ \_ \\ Software \\ Klassen \\ für lokale Computer
-   HKEY- \_ Benutzer- \\ \* \\ Software \\ Klassen \\ CLSID
-   Schnittstelle für HKEY- \_ Benutzer- \\ \* \\ Software \\ Klassen \\
-   HKEY- \_ Benutzer \\ \* \_ Klassen \\ CLSID
-   \_ \\ \* \_ Klassen \\ Schnittstelle für HKEY-Benutzer

Sie werden verwendet, um die Daten beizubehalten, die von 32-Bit-und 64-Bit-Anwendungen nicht gemeinsam verwendet werden sollen.

## <a name="manifestation"></a>Ausstrahlung

CLSID-und Schnittstellen Schlüssel aus der obigen Liste werden nicht mehr angezeigt, wenn Sie noch umgeleitet werden. Obwohl dies das gewünschte Verhalten in den meisten Fällen ist, kann es vorkommen, dass Anwendungen eine Abhängigkeit von Ihrem reflektierten Verhalten in Vista annehmen können.

Die Funktionen, mit denen Anwendungen die Reflektion steuern können (regdisablereflectionkey und regenablereflectionkey), sind in Windows 7 nicht funktionsfähig.

## <a name="mitigation-of-impact"></a>Minderung der Auswirkung

COM ist der größte Consumer der Registrierungs Reflektion. COM und andere Consumer wurden aktualisiert, um dieser Änderung Rechnung zu tragen. Diese Änderung wirkt sich nicht auf Anwendungen aus, die com-Standard-APIs verwenden.

## <a name="solution"></a>Lösung

Wenden Sie eine der folgenden Optionen an, wenn Sie sich für die Synchronisierung von 32-Bit-und 64-Bit-Ansichten auf die Registrierung der

-   Erstellen Sie während der Installation explizit Schlüssel in beiden Ansichten.
-   Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel
-   Überprüfen Sie beim Abfragen eines reflektierten Schlüssels beide Sichten der Registrierung.

    **Hinweis:** Key \_ WOW64 \_ 32key und Key \_ WOW64 \_ 64 Schlüsselflags können nicht kombiniert werden.

Wenden Sie eine der folgenden Optionen an, wenn Sie sich auf regdisablereflectionkey-Funktionen verlassen, um die Registrierungs Reflektion zu deaktivieren:

-   Erstellen Sie während der Installation explizit Schlüssel in beiden Ansichten.
-   Verschieben der Schlüssel aus dem Bereich der reflektierten Schlüssel
-   Verwenden Sie plattformspezifische Unterschlüssel (z. b. x86, amd64 und ia64), um Bitness spezifische Daten zu trennen.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Artikel zur Registrierungs Reflektion](../winprog64/registry-reflection.md)
-   [Liste mit umgeleiteten Schlüsseln im Artikel zum Registrierungs Redirector](../winprog64/registry-redirector.md)
-   [Bewährte Methoden für WOW64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.

 

 

 
