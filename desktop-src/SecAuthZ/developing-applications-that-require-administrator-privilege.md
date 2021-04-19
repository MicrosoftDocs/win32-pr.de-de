---
description: Es ist möglich, eine Anwendung zu entwickeln, die Vorgänge ausführt, für die Administratorrechte erforderlich sind, aber noch als Standardbenutzer ausgeführt werden.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363633"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind

Es ist möglich, eine Anwendung zu entwickeln, die Vorgänge ausführt, für die Administratorrechte erforderlich sind, aber noch als Standardbenutzer ausgeführt werden.

Es gibt mehrere Modelle, um dies zu erreichen.



| Thema                                                                | BESCHREIBUNG                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modell mit erhöhten Rechten](elevated-task-model.md)                       | Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.                                                                     |
| [Betriebs System-Dienstmodell](operating-system-service-model.md) | Eine Anwendung, die als Standardbenutzer ausgeführt wird, kommuniziert mithilfe eines [Remote Prozedur Aufrufs](/windows/desktop/Rpc/rpc-start-page) (RPC) mit einem Dienst, der als **System** ausgeführt wird.                                              |
| [Administrator Broker Modell](administrator-broker-model.md)         | Die Anwendung ist in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, und die andere wird mit Administrator Berechtigungen ausgeführt.                                                          |
| [COM-Objektmodell für Administratoren](administrator-com-object-model.md) | Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem ein Objekt mit [Component Object Model](/windows/desktop/com/component-object-model--com--portal) erhöhten Rechten erstellt wird. |



 

 

 
