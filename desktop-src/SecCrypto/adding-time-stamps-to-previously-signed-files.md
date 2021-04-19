---
description: Zeitstempel werden normalerweise eingeschlossen, wenn eine Datei mithilfe von SignTool mit der Option-t signiert wird.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Hinzufügen von Zeitstempeln zu zuvor signierten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106367338"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Hinzufügen von Zeitstempeln zu zuvor signierten Dateien

Zeitstempel werden normalerweise eingeschlossen, wenn eine Datei mithilfe von SignTool mit der Option **-t** signiert wird. Außerdem können Zeitstempel zu Dateien hinzugefügt werden, die ohne einen Zeitstempel signiert wurden. Mit dem folgenden Befehl wird einer zuvor signierten Datei ein Zeitstempel hinzugefügt:

**SignTool Zeitstempel-t https: \/ /timestamp.Digicert.com *MyControl.exe***

> [!Note]  
> Die Datei, die mit einem Zeitstempel versehen werden soll, muss bereits signiert sein.

 

Weitere Informationen zu SignTool finden Sie unter [SignTool](signtool.md).

 

 



