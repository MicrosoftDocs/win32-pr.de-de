---
description: Verwalten sie die Freigabe von Assemblys und die DLL-Versionsverwaltung in den Systemen parallel zum Assemblyspeicher aus Programmen. Schreiben Sie Assemblymanifeste und selbstbeschreibende Anwendungen für die Freigabe von Assemblys und das Umleiten von DLLs.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Isolierte Anwendungen und parallele Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af477178aa3fd68563ee53017d80c00e103b4cb97a6fd16062d307375b29574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127490"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Isolierte Anwendungen und parallele Assemblys

## <a name="purpose"></a>Zweck

Isolierte Anwendungen und parallele Assemblys ist eine Microsoft Windows-Lösung, die Versionskonflikte in Windows-Clientanwendungen reduziert. Mit Windows können Anwendungsentwickler isolierte Anwendungen erstellen, die vollständig selbstbeschreibend sind und von Änderungen an der Registrierung, anderen Anwendungen oder anderen Versionen von Assemblys, die auf dem System ausgeführt werden, nicht betroffen sind. Anwendungsautoren und -administratoren können Manifeste verwenden, um die Freigabe von assemblys nach der Bereitstellung entweder global oder anwendungsbezogen zu verwalten. Kunden profitieren von isolierten Anwendungen, die stabiler und zuverlässiger aktualisiert werden.

## <a name="where-applicable"></a>Anwendungsbereich

Isolierte Anwendungen und die übergreifende Assemblyfreigabe können verwendet werden, um Anwendungen zu entwickeln, die Betriebssystemassemblys sicher gemeinsam nutzen. Entwickler können diese Technologie verwenden, um Dll-Versionskonflikte zu beheben, die durch eine inkompatible Version einer freigegebenen Assembly verursacht werden.

Wenn Ihre Anwendung konsistent die Version einer getesteten Komponente abrufen muss, ist es möglich, ihre Anwendung zu isolieren, sodass sie immer mit der getesteten Version der Komponente auf dem Computer des Benutzers ausgeführt wird.

Isolierte Anwendungen und side-by-side-Assemblys sind für die Entwicklung von Desktopanwendungen vorgesehen.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Dokumentation richtet sich in erster Linie an Softwareentwickler, Anwendungsentwickler und Netzwerkadministratoren:

-   Softwareentwickler, die isolierte Anwendungen erstellen möchten, die die von Microsoft und anderen Verlegern von Nebenassemblys zur Verfügung gestellten assemblyseitigen Assemblys verwenden.
-   Anwendungsentwickler, die daran interessiert sind, ihre eigenen parallelen Assemblys zu erstellen, um ihre Anwendungen zu isolieren.
-   Netzwerkadministratoren, die weitere Informationen zu isolierten Anwendungen benötigen.

Als primäre Referenz für die gemeinsame Nutzung von nebeneinander und isolierten Anwendungen bietet diese Dokumentation allgemeine Hintergrundinformationen zum Erstellen von Manifesten und nebenseitigen Assemblys, installieren isolierter Anwendungen und nebeneinander ausgeführter Assemblys sowie zur Verwendung der Aktivierungskontext-API.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Windows Server 2003 und höher oder Windows XP und höher ist erforderlich, um assemblys und Manifeste nebeneinander zu verwenden, um Anwendungen zu isolieren und die Aktivierungskontext-API zu verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                         | Beschreibung                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Referenz](side-by-side-assemblies-reference.md)<br/> | Dokumentation zu isolierten Anwendungen und nebenseitigen Assemblys.<br/> |



 

 

 




