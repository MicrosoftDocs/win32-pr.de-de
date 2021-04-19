---
description: Eine TAPI-Anwendung muss einen Initialisierungs Vorgang aufzurufen, der eine Reihe von Aktionen von TAPI und den Dienstanbietern auffordert, die die Kommunikationsumgebung für die Anwendung einrichten.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Primäre Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350014"
---
# <a name="primary-initialization"></a>Primäre Initialisierung

Eine TAPI-Anwendung muss einen Initialisierungs Vorgang aufzurufen, der eine Reihe von Aktionen von TAPI und den Dienstanbietern auffordert, die die Kommunikationsumgebung für die Anwendung einrichten.

-   Die Initialisierung ist synchron und wird erst zurückgegeben, wenn der Vorgang beendet wurde oder fehlgeschlagen ist.
-   Wenn tapisrv nicht bereits ausgeführt wird, wird es von TAPI gestartet.
-   TAPI richtet eine Verbindung mit dem tapisrv-Prozess ein.
-   TAPISVR lädt die in der Registrierung angegebenen Dienstanbieter und fordert Sie auf, die von Ihnen unterstützten Geräte zu initialisieren.

**TAPI 2. x:** Anwendungen führen die Initialisierung durch Aufrufen von [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)durch.

**TAPI 3. x:** Anwendungen nennen [**ittapi:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).

 

 
