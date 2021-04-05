---
title: Auswirkungen der Sicherheit bei der Suche
description: Sicherheit ist ein impliziter Filter beim Durchführen von Such Vorgängen, beim Auflisten von Containern oder beim Lesen von Eigenschaften.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- Auswirkungen der Sicherheit beim Suchen Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707698"
---
# <a name="effects-of-security-on-searching"></a>Auswirkungen der Sicherheit bei der Suche

Sicherheit ist ein impliziter Filter beim Durchführen von Such Vorgängen, beim Auflisten von Containern oder beim Lesen von Eigenschaften.

ADSI kann keine \_ solche \_ Eigenschaft oder keine \_ derartigen \_ Objekt Fehler zurückgeben, auch wenn das Objekt vorhanden ist, wenn Sie keinen Zugriff auf die Lese Attribute für das Objekt haben.

Beispielsweise kann ein Aufrufer in der Lage sein, die untergeordneten Objekte in einem Container aufzulisten, da der Aufrufer \_ überlisten Inhalts Rechte für den Container verfügt. Der gleiche Aufrufer ist jedoch möglicherweise nicht in der Lage, auf die aufgelisteten Objekte zuzugreifen, wenn der Aufrufer keinen Lesezugriff auf die untergeordneten Objekte hat. In diesem Fall gibt eine Abfrage für ein untergeordnetes Objekt möglicherweise kein \_ solches Objekt zurück, \_ auch wenn der Aufrufer das Objekt erfolgreich aufzählt.

Wenn der Aufrufer nicht über ausreichende Rechte verfügt, können die folgenden Rückgabecodes zurückgegeben werden:

E \_ ADS \_ ungültiges \_ Domänen \_ Objekt

E \_ ADS- \_ Eigenschaft \_ nicht \_ unterstützt

E \_ ADS- \_ Eigenschaft \_ nicht \_ gefunden

 

 




