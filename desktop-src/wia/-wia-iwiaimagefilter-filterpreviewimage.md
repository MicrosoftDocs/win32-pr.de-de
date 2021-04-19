---
description: Filtert das Vorschaubild.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'Iwiaimagefilter:: FilterPreviewImage-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346999"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>Iwiaimagefilter:: FilterPreviewImage-Methode

Filtert das Vorschaubild.

## <a name="syntax"></a>Syntax


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Nicht verwendet. Auf 0 festlegen.

</dd> <dt>

*pWiaChildItem2* \[ in\]
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Das Element, das verarbeitet wird.

</dd> <dt>

_InputImageExtents * \[ in\]
</dt> <dd>

Typ: **Rect**

Die Koordinaten (auf dem physischen Erwerbs Bereich) des Bilds, das von der Vorschau Komponente intern zwischengespeichert wird.

</dd> <dt>

*pinputstream* \[ in\]
</dt> <dd>

Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Ein Zeiger auf die [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle für die zwischengespeicherten Bilddaten, die gefiltert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nennen Sie diese Methode nicht direkt aus der Anwendung.

*pWiaChildItem2* muss ein untergeordnetes Element des *pWiaItem2* sein, das an [**iwiaimagefilter:: initializefilter**](-wia-iwiaimagefilter-initializefilter.md)übermittelt wurde.

*Inputimageextents* ist erforderlich, da der Bild Verarbeitungs Filter dafür zuständig ist, den Bildbereich auszulagern, den *pWiaChildItem2* aus den durch *pinputstream* weiter gegebenen Bilddaten repräsentiert.

Eine Anwendung muss sicherstellen, dass *pWiaChildItem2* das gleiche Bildformat (WIA \_ IPA \_ -Format), Auflösung (WIA \_ \_ -IPS-xres und WIA- \_ IPS \_ ) und Bittiefe (WIA \_ IPA- \_ Tiefe) wie *pWiaItem2* bei der Übergabe an [**getnewpreview**](-wia-iwiapreview-getnewpreview.md)aufweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
