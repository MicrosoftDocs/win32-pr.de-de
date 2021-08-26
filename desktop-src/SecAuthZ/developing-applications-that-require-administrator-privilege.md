---
description: Es ist möglich, eine Anwendung zu entwickeln, die Vorgänge ausführt, die Administratorberechtigungen erfordern, aber als Standardbenutzer ausgeführt werden.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Entwickeln von Anwendungen, die Administratorrechte erfordern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dc8ea112cfec6297cf7c11a044e62695a24e93d7eb0b13a773d40acd6c6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994430"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Entwickeln von Anwendungen, die Administratorrechte erfordern

Es ist möglich, eine Anwendung zu entwickeln, die Vorgänge ausführt, die Administratorberechtigungen erfordern, aber als Standardbenutzer ausgeführt werden.

Es gibt mehrere Modelle, um dies zu erreichen.



| Thema                                                                | BESCHREIBUNG                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aufgabenmodell mit erhöhten Rechten](elevated-task-model.md)                       | Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.                                                                     |
| [Betriebssystemdienstmodell](operating-system-service-model.md) | Eine Anwendung, die als Standardbenutzer ausgeführt wird, kommuniziert mit einem Dienst, der als **SYSTEM** ausgeführt wird, mithilfe von [REMOTE PROCEDURE CALL](/windows/desktop/Rpc/rpc-start-page) (RPC).                                              |
| [Administrator Broker-Modell](administrator-broker-model.md)         | Die Anwendung ist in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, das andere mit Administratorrechten.                                                          |
| [COM-Objektmodell des Administrators](administrator-com-object-model.md) | Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, für die Administratorrechte erforderlich sind, indem ein Objekt mit erhöhten [Component Object Model](/windows/desktop/com/component-object-model--com--portal) erstellt wird. |



 

 

 
