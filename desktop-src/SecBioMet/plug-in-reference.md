---
title: Plug-in-Referenz
description: Adapter Funktionen, Wrapper Funktionen und Strukturen zum Erstellen von benutzerdefinierten Plug-in-Adaptern von drei Typen Engine, Sensor und Storage.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API Windows-Biometrieframework API für Windows-Biometrieframework API, Plug-in-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471701"
---
# <a name="plug-in-reference"></a>Plug-in-Referenz

Biometrische Geräte werden in einer Vielzahl von Typen und Konfigurationen gefertigt. Der Windows-Biometrieframework enthält eine erweiterbare Architektur, die es Ihnen ermöglicht, diese Vielfalt durch das Erstellen von benutzerdefinierten Plug-ins zu behandeln. Im Mittelpunkt dieser Architektur befindet sich ein Software Objekt, das als biometrische Einheit bezeichnet wird. Sie können sich eine biometrische Einheit als Abstraktion vorstellen, die ein biometrisches Gerät für das Framework darstellt. Plug-in-Softwarekomponenten, die als Adapter bezeichnet werden, verbinden die biometrische Einheit mit der zugeordneten Hardware. Es gibt drei Arten von Adaptern, die Sie erstellen können. Ein Engine-Adapter generiert biometrische Vorlagen aus aufgezeichneten Beispielen, entspricht Beispielen für vorhandene Vorlagen und Index Vorlagen. Ein Sensor Adapter dient als Wrapper für ein biometrisches Gerät und stellt eine Standardschnittstelle zum Konfigurieren des Sensors, zum Erfassen von Beispielen und zum Steuern des Flusses biometrischer Daten an die Verarbeitungs-Engine bereit. Ein Speicher Adapter verwaltet Vorlagen Datenbanken.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Plug-in-Funktionen](plug-in-functions.md)<br/>                 | Funktionen, die Sie verwenden können, um die Adapter-Plug-ins zu erstellen, die eine biometrische Einheit bilden.<br/>                                                                     |
| [Plug-in-Strukturen](plug-in-structures.md)<br/>               | Strukturen für die Entwicklung von Client Anwendungen durch die Windows-Biometrieframework-API.<br/>                                                                   |
| [Plug-in-Wrapper Funktionen](plug-in-wrapper-functions.md)<br/> | Wrapper Funktionen, die es Ihnen ermöglichen, eine öffentliche Funktion auf jedem Adapter aufzurufen, der an die Pipeline angefügt ist, ohne manuell einen Zeiger auf den Adapter zu beschaffen.<br/> |



 

 

 





