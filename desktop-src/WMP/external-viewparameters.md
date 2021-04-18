---
title: Extern. viewparameters
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. viewparameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Externe. viewparameters-Fenster Media Player
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364724"
---
# <a name="externalviewparameters"></a>Extern. viewparameters

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **viewparameters** -Eigenschaft ruft Parameter ab, die der aktuellen Ansicht in Windows Media Player zugeordnet sind.

## <a name="syntax"></a>Syntax

**Window. extern. viewparameters**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft gibt eine schreibgeschützte **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ruft Parameter ab, die zuvor vom Onlinespeicher festgelegt wurden. Der Online Shop kann z. b. Ansichts Parameter im *viewparameame-* Parameter der [changeView](external-changeview.md) -Methode oder im Parameter *para* meters der [changeviewonlinelist](external-changeviewonlinelist.md) -Methode angeben.

Sicht Parameter werden von Windows Media Player nicht interpretiert. Sie werden vom Online Shop erstellt und sind nur für den Online Shop von Bedeutung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





