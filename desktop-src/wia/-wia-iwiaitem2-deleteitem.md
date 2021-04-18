---
description: Entfernt das aktuelle IWiaItem2-Objekt aus der Objektstruktur des Geräts.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: IWiaItem2::D eleteitem-Methode (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368096"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2::D eleteitem-Methode

Entfernt das aktuelle [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt aus der Objektstruktur des Geräts.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das Windows Image Acquisition (WIA) 2,0-Laufzeitsystem stellt jedes WIA 2,0-Hardware Gerät dar, das mit dem Computer des Benutzers verbunden ist, als hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten. Ein bestimmtes WIA 2,0-Gerät lässt möglicherweise zu, dass Anwendungen **IWiaItem2** -Objekte aus der Struktur löschen. Elemente mit untergeordneten Elementen können nicht gelöscht werden. Die [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle muss verwendet werden, um das Gerät für das Löschen von Elementen abzufragen.

Wenn das Gerät das Löschen von Elementen in seiner [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur unterstützt, müssen Sie die **IWiaItem2::D eleteitem** -Methode zum Entfernen des **IWiaItem2** -Objekts aufzurufen. Beachten Sie, dass diese Methode nur ein Objekt löscht, nachdem alle Verweise auf das Objekt freigegeben wurden. Wenn beim Löschen eines Elements ein Fehler aufgetreten ist, \_ wird "E DeleteItem" zurückgegeben. Der numerische Wert für diesen Fehler ist noch nicht definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




