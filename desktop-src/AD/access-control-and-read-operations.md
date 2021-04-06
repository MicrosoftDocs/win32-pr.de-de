---
title: Access Control-und Lesevorgänge
description: Sicherheit ist ein impliziter Filter zum Suchen, Aufzählen von Containern oder zum Lesen von Eigenschaften.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Access Control-und Lesevorgänge (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036265"
---
# <a name="access-control-and-read-operations"></a>Access Control-und Lesevorgänge

Sicherheit ist ein impliziter Filter zum Suchen, Aufzählen von Containern oder zum Lesen von Eigenschaften. Wenn Sie nicht über die erforderlichen Zugriffsrechte verfügen, kann der Versuch, Objekte oder Leseeigenschaften aufzulisten, mit den folgenden Fehlercodes fehlschlagen, auch wenn das Objekt oder die Eigenschaft vorhanden ist:

-   **E \_ ADS \_ ungültiges \_ Domänen \_ Objekt**
-   **E \_ ADS- \_ Eigenschaft \_ nicht \_ unterstützt**
-   **E \_ ADS- \_ Eigenschaft \_ nicht \_ gefunden**

Beachten Sie, dass ein Aufrufer mit dem **AD \_ right \_ actrl \_ DS \_** -Zugriff auf einen Container die untergeordneten Objekte im Container aufzählen kann. Der Versuch, auf ein untergeordnetes Objekt zuzugreifen, kann jedoch weiterhin einen Fehler verursachen, z. b. ein **\_ \_ unbekanntes \_ Objekt** , wenn der **Aufrufer keinen Ad \_ right \_ actrl \_ DS- \_ Listen \_ Objekt** Zugriff auf das untergeordnete Objekt hat.

Die Auswirkung der Sicherheit auf Lesevorgänge wird nicht notwendigerweise als Fehler dargestellt. Beispielsweise kann ein Suchvorgang erfolgreich ausgeführt werden, die Suchergebnisse enthalten jedoch keine Objekte oder Eigenschaften, auf die der Aufrufer keinen Zugriff hat.

 

 




