---
title: Schema (AD DS)
description: Active Directory Schema ist als Satz von Objektklassen Instanzen implementiert, die im Verzeichnis gespeichert werden.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory Schema Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "103719884"
---
# <a name="schema-ad-ds"></a>Schema (AD DS)

Active Directory Schema ist als Satz von Objektklassen Instanzen implementiert, die im Verzeichnis gespeichert werden. Dies unterscheidet sich sehr von vielen Verzeichnissen, die über ein Schema verfügen, aber als Textdatei gespeichert werden, die beim Start gelesen wird. Das Speichern des Schemas im Verzeichnis hat viele Vorteile. Benutzer Anwendungen können diese z. b. lesen, um zu ermitteln, welche Objekte und Eigenschaften verfügbar sind.

Active Directory Schema kann dynamisch aktualisiert werden. Das heißt, eine Anwendung kann das Schema mit neuen Attributen und Klassen erweitern und die Erweiterungen sofort verwenden. Schema Aktualisierungen werden erreicht, indem die im Verzeichnis gespeicherten Schema Objekte erstellt oder geändert werden. Wie jedes Objekt in Active Directory schützen Zugriffs Steuerungs Listen (ACLs) Schema Objekte, sodass autorisierte Benutzer das Schema nur ändern können.

Weitere Informationen finden Sie unter [Active Directory Schema](active-directory-schema.md).

 

 




