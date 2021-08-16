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

Diese Aktion muss vor dem Assistenten für die Benutzeroberfläche in der [Tabelle InstallUISequence](installuisequence-table.md) und vor der [Aktion RegisterUser](registeruser-action.md) in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)sequenziert werden.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Das Installationsprogramm überprüft durch Überprüfen der [**ProductID-Eigenschaft,**](productid.md) ob ein Produkt erfolgreich überprüft wurde. Das Installationsprogramm legt die **ProductID-Eigenschaft** nach einer erfolgreichen Überprüfung auf den vollständigen Produktbezeichner fest. Die ValidateProductID-Aktion führt keine Aktion aus, wenn die **ProductID-Eigenschaft** bereits durch eine erfolgreiche Validierung oder eine andere Methode festgelegt wurde.

Die ValidateProductID-Aktion gibt immer einen Erfolg zurück, unabhängig davon, ob der Produktbezeichner gültig ist, sodass der Produktbezeichner bei der ersten Ausführung des Produkts in die Befehlszeile eingegeben werden kann.

Der Produktbezeichner kann überprüft werden, ohne dass der Benutzer diese Informationen erneut eingibt, indem die [**PIDKEY-Eigenschaft**](pidkey.md) in der Befehlszeile oder mithilfe einer Transformation festgelegt wird. Die Anzeige des Dialogfelds, in dem der Benutzer aufgefordert wird, den Produktbezeichner einzugeben, kann dann davon abhängig gemacht werden, dass die [**ProductID-Eigenschaft**](productid.md) vorhanden ist, die festgelegt wird, wenn die **PIDKEY-Eigenschaft** überprüft wird.

 

 



