---
description: Entfernt das aktuelle IWiaItem2-Objekt aus der Objektstruktur des Geräts.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: IWiaItem2::D eleteItem-Methode (Wia.h)
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
ms.openlocfilehash: 791d596ee48c4d3e2efd67259ec2e37249c930c6da32f704d332df1da6930503
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593000"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2::D eleteItem-Methode

Entfernt das aktuelle [**IWiaItem2-Objekt**](-wia-iwiaitem2.md) aus der Objektstruktur des Geräts.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das WIA 2.0-Laufzeitsystem (Windows Image Acquisition) stellt jedes WIA 2.0-Hardwaregerät dar, das mit dem Computer des Benutzers verbunden ist, als hierarchische Struktur von [**IWiaItem2-Objekten.**](-wia-iwiaitem2.md) Ein bestimmtes WIA 2.0-Gerät lässt möglicherweise zu, dass Anwendungen **IWiaItem2-Objekte** aus der Struktur löschen. Elemente, die über children verfügen, können nicht gelöscht werden. Die [**IEnumWIA \_ DEV \_ CAPS-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) muss verwendet werden, um das Gerät auf die Funktion zum Löschen von Element zu fragen.

Wenn das Gerät das Löschen von Element in der [**IWiaItem2-Struktur**](-wia-iwiaitem2.md) unterstützt, rufen Sie die **IWiaItem2::D eleteItem-Methode** auf, um das **IWiaItem2-Objekt** zu entfernen. Beachten Sie, dass diese Methode ein Objekt erst löscht, nachdem alle Verweise auf das Objekt freigegeben wurden. Wenn beim Löschen eines Elements ein Fehler auft ist, wird E \_ DELETEITEM zurückgegeben. Der numerische Wert für diesen Fehler ist noch nicht definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




