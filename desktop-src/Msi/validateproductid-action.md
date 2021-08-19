---
description: Die ValidateProductID-Aktion legt die ProductID-Eigenschaft auf den vollständigen Produktbezeichner fest.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: ValidateProductID-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be241bddbafb8f963aea1e73a2750c9d45766eb06767b0b30142883fa1bcebac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942230"
---
# <a name="validateproductid-action"></a>ValidateProductID-Aktion

Die ValidateProductID-Aktion legt die [**ProductID-Eigenschaft**](productid.md) auf den vollständigen Produktbezeichner fest.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Diese Aktion muss vor dem Benutzeroberflächen-Assistenten in der [InstallUISequence-Tabelle](installuisequence-table.md) und vor der [RegisterUser-Aktion](registeruser-action.md) in der [InstallExecuteSequence-Tabelle sequenziert werden.](installexecutesequence-table.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

Das Installationsprogramm überprüft, ob ein Produkt erfolgreich überprüft wurde, indem die [**ProductID-Eigenschaft**](productid.md) überprüft wird. Das Installationsprogramm legt die **ProductID-Eigenschaft** nach einer erfolgreichen Überprüfung auf den vollständigen Produktbezeichner fest. Die ValidateProductID-Aktion führt nichts aus, wenn **die ProductID-Eigenschaft** bereits durch eine erfolgreiche Validierung oder durch eine andere Methode festgelegt wurde.

Die ValidateProductID-Aktion gibt immer einen Erfolg zurück, unabhängig davon, ob der Produktbezeichner gültig ist, sodass der Produktbezeichner bei der ersten Ausführung des Produkts in die Befehlszeile eingegeben werden kann.

Der Produktbezeichner kann überprüft werden, ohne dass der Benutzer diese Informationen erneut eintipen muss, indem die [**PIDKEY-Eigenschaft**](pidkey.md) in der Befehlszeile oder mithilfe einer Transformation angegeben wird. Die Anzeige des Dialogfelds, in dem der Benutzer zur Eingabe des Produktbezeichners aufgefordert wird, kann dann vom Vorhandensein der [**ProductID-Eigenschaft**](productid.md) abhängig gemacht werden, die festgelegt wird, wenn die **PIDKEY-Eigenschaft** überprüft wird.

 

 



