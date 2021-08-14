---
title: Auswirkungen der Sicherheit auf die Suche
description: Sicherheit ist ein impliziter Filter beim Ausführen von Suchvorgängen, beim Aufzählen von Containern oder beim Lesen von Eigenschaften.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- Auswirkungen der Sicherheit auf die Suche in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 429150489f2ab4d00015744beff72ee2b90b0399afd3d43f9263d39cadbaecd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191620"
---
# <a name="effects-of-security-on-searching"></a>Auswirkungen der Sicherheit auf die Suche

Sicherheit ist ein impliziter Filter beim Ausführen von Suchvorgängen, beim Aufzählen von Containern oder beim Lesen von Eigenschaften.

ADSI kann NO SUCH PROPERTY- oder NO SUCH OBJECT-Fehler zurückgeben, auch wenn das Objekt vorhanden ist, wenn Sie keinen Zugriff auf \_ \_ \_ \_ Leseattribute für das Objekt haben.

Beispielsweise kann ein Aufrufer die untergeordneten Objekte in einem Container auflisten, da der Aufrufer über LIST \_ CONTENTS-Rechte für den Container verfügt. Derselbe Aufrufer kann jedoch möglicherweise nicht auf die aufzählten Objekte zugreifen, wenn der Aufrufer keinen Lesezugriff auf die untergeordneten Objekte hat. In diesem Fall gibt eine Abfrage für ein untergeordnetes Objekt möglicherweise NO SUCH OBJECT zurück, obwohl der Aufrufer das \_ \_ Objekt erfolgreich aufzählt.

Wenn der Aufrufer nicht über ausreichende Rechte verfügt, werden möglicherweise die folgenden Rückgabecodes zurückgegeben:

E \_ ADS \_ INVALID \_ DOMAIN \_ OBJECT

E \_ \_ ADS-EIGENSCHAFT \_ WIRD NICHT \_ UNTERSTÜTZT

E \_ \_ ADS-EIGENSCHAFT \_ NICHT \_ GEFUNDEN

 

 




