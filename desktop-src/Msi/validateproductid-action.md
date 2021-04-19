---
description: Die Aktion "ValidateProductID" legt die ProductID-Eigenschaft auf den vollständigen Produkt Bezeichner fest.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: ValidateProductID-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346995"
---
# <a name="validateproductid-action"></a>ValidateProductID-Aktion

Die Aktion "ValidateProductID" legt die [**ProductID-**](productid.md) Eigenschaft auf den vollständigen Produkt Bezeichner fest.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Diese Aktion muss vor dem Assistenten für die Benutzeroberfläche in der [Tabelle InstallUISequence](installuisequence-table.md) und vor der [RegisterUser-Aktion](registeruser-action.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)sequenziert werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Der Installer überprüft, ob ein Produkt erfolgreich überprüft wurde, indem er die [**ProductID-**](productid.md) Eigenschaft überprüft. Der Installer legt die **ProductID-** Eigenschaft nach einer erfolgreichen Validierung auf den vollständigen Produkt Bezeichner fest. Die Aktion "ValidateProductID" führt keine Aktion aus, wenn die Eigenschaft " **ProductID** " bereits durch eine erfolgreiche Validierung oder eine andere Methode festgelegt wurde.

Die Aktion "ValidateProductID" gibt immer einen Erfolg zurück, unabhängig davon, ob der Produkt Bezeichner gültig ist, sodass der Product Identifier in der Befehlszeile eingegeben werden kann, wenn das Produkt zum ersten Mal ausgeführt wird.

Der Produkt Bezeichner kann überprüft werden, ohne dass der Benutzer diese Informationen erneut eingeben muss, indem er die [**PIDKEY**](pidkey.md) -Eigenschaft in der Befehlszeile oder mithilfe einer Transformation festlegt. Die Anzeige des Dialog Felds, das den Benutzer zur Eingabe des Produkt Bezeichners anfordert, kann dann bedingt beim vorhanden sein der [**ProductID-**](productid.md) Eigenschaft festgelegt werden, die beim Validieren der **PIDKEY** -Eigenschaft festgelegt wird.

 

 



