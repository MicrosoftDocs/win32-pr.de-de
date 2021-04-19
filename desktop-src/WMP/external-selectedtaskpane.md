---
title: Extern. selectedtaskpane
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die selectedtaskpane-Eigenschaft gibt den aktuell ausgewählten Aufgabenbereich an oder ruft ihn ab.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Externe. selectedtaskpane-Fenster Media Player
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355274"
---
# <a name="externalselectedtaskpane"></a>Extern. selectedtaskpane

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **selectedtaskpane** -Eigenschaft gibt den aktuell ausgewählten Aufgabenbereich an oder ruft ihn ab.

## <a name="syntax"></a>Syntax

Window. extern. selectedtaskpane = *Servicetask*

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**. Mögliche Werte sind "ServiceTask1", "ServiceTask2" und "ServiceTask3".

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Wert für diese Eigenschaft angeben, wird die Schaltfläche für diesen Bereich hervorgehoben. Der angegebene Aufgabenbereich wird nicht aktiv. Geben Sie einen Wert für diese Eigenschaft an, um die aktuelle Aufgabenbereichs Schaltfläche für die Webseite festzulegen, wenn die Seite geladen wird, um sicherzustellen, dass die Schaltfläche korrekter Aufgabenbereich aktiv ist.

Um einen bestimmten Aufgabenbereich als aktiven Bereich festzulegen, verwenden Sie die **navigatetaskpaneurl** -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 2-Online Speicher**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Extern. navigatetaskpaneurl**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





