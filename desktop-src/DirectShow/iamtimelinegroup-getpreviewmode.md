---
description: Die getpreviewmode-Methode ruft den Vorschaumodus für die Gruppe ab.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'Iamtimelinegroup:: getpreviewmode-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354838"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a>Iamtimelinegroup:: getpreviewmode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetPreviewMode` Methode ruft den Vorschaumodus für die Gruppe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfpreview* 
</dt> <dd>

Empfängt einen booleschen Wert, der den Vorschaumodus angibt. **True** gibt an, dass sich die Gruppe im Vorschaumodus befindet. Wenn der Wert **false** ist, befindet sich die Gruppe im Erstellungs Modus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Im Vorschaumodus werden Frames bei langsamen Effekten oder Übergängen gelöscht, damit das Video mit dem Audioformat synchronisiert wird. Das Video könnte als Ergebnis aussehen. Im Erstellungs Modus wird jeder Frame gerendert. Der Erstellungs Modus eignet sich zum Schreiben von Dateien. bei der Bildschirm Vorschau wird das Video möglicherweise nicht mehr mit dem Audioformat synchronisiert.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinegroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




