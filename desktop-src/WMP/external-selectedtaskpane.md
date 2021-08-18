---
title: External.SelectedTaskPane
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die SelectedTaskPane-Eigenschaft gibt den aktuell ausgewählten Aufgabenbereich an oder ruft den Taskbereich ab.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- External.SelectedTaskPane-Windows Media Player
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
ms.openlocfilehash: 24e49225be7bbdb5ce128a793d3c88409ef9d994ef5017c57b5f12738b62eaa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736190"
---
# <a name="externalselectedtaskpane"></a>External.SelectedTaskPane

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **SelectedTaskPane-Eigenschaft** gibt den aktuell ausgewählten Aufgabenbereich an oder ruft den Taskbereich ab.

## <a name="syntax"></a>Syntax

window.external.SelectedTaskPane = *servicetask*

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine **Zeichenfolge** mit Lese-/Schreibzugriff. Mögliche Werte sind "ServiceTask1", "ServiceTask2" und "ServiceTask3".

## <a name="remarks"></a>Hinweise

Wenn Sie einen Wert für diese Eigenschaft angeben, wird die Schaltfläche für diesen Bereich hervorgehoben. Der angegebene Aufgabenbereich wird nicht aktiviert. Sie sollten einen Wert für diese Eigenschaft angeben, um die aktuelle Aufgabenbereichsschaltfläche für Ihre Webseite festzulegen, wenn die Seite geladen wird, um sicherzustellen, dass die richtige Aufgabenbereichsschaltfläche aktiv ist.

Um einen bestimmten Aufgabenbereich zum aktiven Aufgabenbereich zu machen, verwenden Sie die **NavigateTaskPaneURL-Methode.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Externes Objekt für Onlineshops vom Typ 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





