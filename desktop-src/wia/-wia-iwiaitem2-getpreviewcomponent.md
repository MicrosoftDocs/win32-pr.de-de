---
description: Ruft die Windows-Abbild Erwerbs-Vorschau Komponente (WIA) 2,0 ab.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2:: getpreviewcomponent-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129421"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>IWiaItem2:: getpreviewcomponent-Methode

Ruft die Windows-Abbild Erwerbs-Vorschau Komponente (WIA) 2,0 ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Nicht verwendet. Auf 0 festlegen.

</dd> <dt>

*ppwiapreview* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **iwiapreview**](-wia-iwiapreview.md)\*\***

Gibt die Adresse eines Zeigers auf die [**iwiapreview**](-wia-iwiapreview.md) -Schnittstelle der vorschaukomponente zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion, um einen Zeiger auf die Adresse der WIA 2,0-Vorschau Komponente für ein beliebiges [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der Objektstruktur eines WIA 2,0-Hardware Geräts zurückzugeben.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den Parameter *ppwiapreview* empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**Iwiapreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
