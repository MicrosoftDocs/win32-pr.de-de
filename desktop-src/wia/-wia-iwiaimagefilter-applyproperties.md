---
description: Ermöglicht dem Bild Verarbeitungs Filter das Zurückschreiben von Eigenschaften an den Treiber (und das Gerät).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Iwiaimagefilter:: applyproperties-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347375"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>Iwiaimagefilter:: applyproperties-Methode

Ermöglicht dem Bild Verarbeitungs Filter das Zurückschreiben von Eigenschaften an den Treiber (und das Gerät).

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwiapropertystorage* \[ in\]
</dt> <dd>

Typ: **[**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _

Gibt einen Zeiger auf den [_ *iwiapropertystorage* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) für die anzuwendenden Eigenschaften an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nennen Sie diese Methode nicht direkt aus der Anwendung. Sie wird von der Windows-Abbild Beschaffung (WIA) 2,0 aufgerufen, nachdem der Bild Verarbeitungs Filter die Rohdaten verarbeitet hat.

*pwiapropertystorage* ist die Schnittstelle [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , in der der Bild Verarbeitungs Filtereigenschaften schreiben soll. Ein Bild Verarbeitungs Filter sollte nur die Methode [IPropertyStorage:: schreitemultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) zum Schreiben von Eigenschaften verwenden.

Diese Methode ermöglicht dem Bild Verarbeitungs Filter das Zurückschreiben von Eigenschaften an den Treiber (und das Gerät). Dies kann für Filter notwendig sein, die Funktionen wie die automatische Verfügbarkeit während der Überprüfung von Filmen implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
