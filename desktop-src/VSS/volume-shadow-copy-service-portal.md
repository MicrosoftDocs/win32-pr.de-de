---
description: Sichern von Volumes, während Anwendungen auf einem System weiterhin auf die Volumes schreiben. Minimieren Sie die Ausfallzeiten der Anwendung, indem Sie schnell eine Momentaufnahme (Schatten Kopie) eines Volumes erstellen, das alle Daten dupliziert. Durchführen einer Sicherung mit mehreren Volumes
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348187"
---
# <a name="volume-shadow-copy-service"></a>Volumeschattenkopie-Dienst

## <a name="purpose"></a>Zweck

Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von COM-Schnittstellen, der ein Framework implementiert, das das Ausführen von Volumesicherungen ermöglicht, während Anwendungen auf einem System weiterhin auf die Volumes schreiben.

Eine Einführung in VSS für Systemadministratoren finden Sie unter [Volumeschattenkopie-Dienst](/windows-server/storage/file-server/volume-shadow-copy-service) in der TechNet-Bibliothek.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

VSS wird unter Microsoft Windows XP und höher unterstützt. Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" in der Dokumentation für dieses Element.

Alle 32-Bit-VSS-Anwendungen (Requester, Anbieter und Writer) müssen als native 32-Bit-oder 64-Bit-Anwendungen ausgeführt werden. Die Ausführung unter WOW64 wird nicht unterstützt. Weitere Informationen finden Sie [unter Unterstützte Konfigurationen und Einschränkungen](usage-conventions.md).

**Windows Server 2003 und Windows XP:** Das Ausführen von 32-Bit-VSS-Anforderern unter WOW64 wird unterstützt, jedoch nicht für Sicherungen des Systemstatus. Das Ausführen von 32-Bit-VSS-Anbietern und-Writern unter WOW64 wird nicht unterstützt. Unterstützung für die Ausführung von 32-Bit-Anforderern unter WOW64 wurde in Windows Vista und nachfolgenden Versionen entfernt.

> [!Note]  
> Eine Schatten Kopie, die auf Windows Server 2003 R2 oder Windows Server 2003 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird. Eine Schatten Kopie, die auf Windows Server 2008 R2 oder Windows Server 2008 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2003 ausgeführt wird. Eine Schatten Kopie, die auf Windows Server 2008 erstellt wurde, kann jedoch auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 ausgeführt wird, und umgekehrt.

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                          | BESCHREIBUNG                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht](volume-shadow-copy-service-overview.md)<br/> | Beschreibt das VSS-Objektmodell, Sicherungs-und Wiederherstellungs Strategien und die Vorgehensweise beim Erstellen von VSS-Anbietern,-Anforderern und-Writern.<br/> |
| [Verweis](volume-shadow-copy-reference.md)<br/>       | Beschreibt VSS-Klassen,-Datentypen,-Enumerationen,-Funktionen,-Schnittstellen und-Strukturen.<br/>                                  |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista und höher            | VSS ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Sie können das SDK für Windows 7 und Windows Server 2008 R2 aus dem [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279)installieren. Sie können auch die [ISO-Version](https://www.microsoft.com/download/details.aspx?id=8442) des SDK aus dem Windows Download Center herunterladen. Frühere Versionen des SDK können von der [Windows SDK Download Seite](https://msdn.microsoft.com/windows/bb980924.aspx)heruntergeladen werden. |
| Windows Server 2003 und Windows XP | VSS ist im SDK für Volumeschattenkopie-Dienst 7,2 verfügbar, das Sie aus dem [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490)herunterladen können. Beachten Sie, dass die 64-Bit-Vssapi. lib-Dateien in den Verzeichnissen unter dem \\ Verzeichnis Win2003 obj für die 64-Bit-Versionen von Windows Server 2003 und Windows XP verwendet werden können.                                                                                                                                                                 |



 

 

 
