---
description: Sichern Sie Volumes, während Anwendungen auf einem System weiterhin auf die Volumes schreiben. Minimieren Sie Ausfallzeiten der Anwendung, indem Sie schnell eine Momentaufnahme (Schattenkopie) eines Volumes erstellen, das alle Daten dupliziert. Ausführen einer Mehrvolumesicherung.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2159d39f407f7ae5dbde454ab6cf3562307d892c
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443081"
---
# <a name="volume-shadow-copy-service"></a>Volumeschattenkopie-Dienst

## <a name="purpose"></a>Zweck

Der Volumeschattenkopie-Dienst (VSS) besteht aus einer Reihe von COM-Schnittstellen, die ein Framework implementieren, damit Volumesicherungen ausgeführt werden können, während Anwendungen auf einem System weiterhin auf die Volumes schreiben.

Eine Einführung in VSS für Systemadministratoren finden Sie unter [Volumeschattenkopie-Dienst](/windows-server/storage/file-server/volume-shadow-copy-service) in der TechNet-Bibliothek.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

VSS wird unter Microsoft Windows XP und höher unterstützt. Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Dokumentation für dieses Element.

Alle 32-Bit-VSS-Anwendungen (Anforderer, Anbieter und Writer) müssen als native 32-Bit- oder 64-Bit-Anwendungen ausgeführt werden. Die Ausführung unter WOW64 wird nicht unterstützt. Weitere Informationen finden Sie unter [Unterstützte Konfigurationen und Einschränkungen.](usage-conventions.md)

**Windows Server 2003 und Windows XP:** Das Ausführen von 32-Bit-VSS-Anforderern unter WOW64 wird unterstützt, jedoch nicht für Systemstatussicherungen. Das Ausführen von 32-Bit-VSS-Anbietern und -Writern unter WOW64 wird nicht unterstützt. Die Unterstützung für die Ausführung von 32-Bit-Anforderern unter WOW64 wurde in Windows Vista und nachfolgenden Versionen entfernt.

> [!Note]  
> Eine Schattenkopie, die unter Windows Server 2003 R2 oder Windows Server 2003 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird. Eine Schattenkopie, die unter Windows Server 2008 R2 oder Windows Server 2008 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2003 ausgeführt wird. Eine Schattenkopie, die unter Windows Server 2008 erstellt wurde, kann jedoch auf einem Computer mit Windows Server 2008 R2 und umgekehrt verwendet werden.

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                          | BESCHREIBUNG                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht](volume-shadow-copy-service-overview.md)<br/> | Beschreibt das VSS-Objektmodell, Sicherungs- und Wiederherstellungsstrategien sowie das Erstellen von VSS-Anbietern, Anforderern und Writern.<br/> |
| [Referenz](volume-shadow-copy-reference.md)<br/>       | Beschreibt VSS-Klassen, -Datentypen, -Enumerationen, -Funktionen, -Schnittstellen und -Strukturen.<br/>                                  |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen



|   Ressource                                 |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista und höher            | VSS ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Sie können das SDK für Windows 7 und Windows Server 2008 R2 im [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279)installieren. Sie können auch die [ISO-Version](https://www.microsoft.com/download/details.aspx?id=8442) des SDK aus dem Windows Download Center herunterladen. Frühere Versionen des SDK können von der [Windows SDK Downloadseite](https://msdn.microsoft.com/windows/bb980924.aspx)heruntergeladen werden. |
| Windows Server 2003 und Windows XP | VSS ist im Volumeschattenkopie-Dienst 7.2 SDK verfügbar, das Sie aus dem [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490)herunterladen können. Beachten Sie, dass die 64-Bit-Dateien vssapi.lib in den Verzeichnissen im \\ Win2003-Obj-Verzeichnis für die 64-Bit-Versionen von Windows Server 2003 und Windows XP verwendet werden können.                                                                                                                                                                 |



 

 

 
