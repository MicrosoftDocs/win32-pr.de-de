---
description: Der Ressourcenschutz verhindert die Ersetzung von Systemdateien und Ordnern sowie Registrierungs Schlüsseln, die für das Betriebssystem von wesentlicher Bedeutung sind. Durch das ändern geschützter Ressourcen können Anwendungs-oder Systemfehler verursacht werden.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Windows-Ressourcenschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347218"
---
# <a name="windows-resource-protection"></a>Windows-Ressourcenschutz

## <a name="purpose"></a>Zweck

Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil des Betriebssystems installiert werden. Es wurde ab Windows Server 2008 und Windows Vista verfügbar. Anwendungen sollten diese Ressourcen nicht überschreiben, da Sie vom System und anderen Anwendungen verwendet werden. Der Schutz dieser Ressourcen verhindert Anwendungs-und Betriebssystem Fehler. WRP ist der neue Name für den Windows-Datei Schutz (WFP). WRP schützt Registrierungsschlüssel und Ordner sowie wichtige Systemdateien.

## <a name="where-applicable"></a>Anwendungsbereich

Alle Windows-basierten Anwendungen und deren Installationsprogramme, die unter Windows Server 2008 oder Windows Vista und höheren Betriebssystemen ausgeführt werden, sollten sich von WRP unterstützen. Alle Windows-basierten Anwendungen, die unter Microsoft Windows Server 2003 oder Windows XP ausgeführt werden, und die zugehörigen Installationsprogramme sollten WFP beachten.

## <a name="developer-audience"></a>Entwicklergruppe

Die WRP-API ist für die Verwendung durch C/C++-Programmierer konzipiert. Die WRP-API verfügt über zwei Funktionen: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) und [**sfciskeyprotected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Anwendungen, die nur die [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) -Funktion verwenden, benötigen Windows Server 2008, Windows Vista, Windows Server 2003 oder Windows XP. Anwendungen, die die [**sfciskeyprotected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) -Funktion verwenden, benötigen Windows Server 2008 oder Windows Vista.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [Informationen zu Windows-Ressourcenschutz](about-windows-file-protection.md)<br/>         | Allgemeine Informationen zu WRP.<br/>   |
| [Windows-Ressourcenschutz Referenz](windows-file-protection-reference.md)<br/> | Referenz Dokumentation für WRP.<br/> |



 

 

 




