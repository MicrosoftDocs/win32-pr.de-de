---
description: Erstellt einen Enumerator von Eigenschafteninformationen für jedes verfügbare Windows WIA 2.0-Gerät (Image Acquisition).
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: IWiaDevMgr2::EnumDeviceInfo-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 8b646c494d9793986373d45db2d89dfde91e744196d86d28aceab35874f504d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208722"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>IWiaDevMgr2::EnumDeviceInfo-Methode

Erstellt einen Enumerator von Eigenschafteninformationen für jedes verfügbare Windows WIA 2.0-Gerät (Image Acquisition).

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt den Typ der zu aufzählenden WIA 2.0-Geräte an.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DEVINFO \_ ENUM \_ LOCAL**


</dt> <dd>

Nur lokal verbundene aktive Scannergeräte werden aufzählt.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DEVINFO \_ ENUM \_ ALL**


</dt> <dd>

Alle Geräte werden sowohl lokal als auch remote aufzählt, einschließlich inaktiver (getrennter) Geräte und legacy-STI-gesteuerte Geräte.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Typ: **[ **IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Empfängt die Adresse eines Zeigers auf die [**IEnumWIA \_ DEV \_ INFO-Schnittstelle.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die **IWiaDevMgr2::EnumDeviceInfo-Methode** erstellt ein Enumeratorobjekt, das die [**IEnumWIA \_ DEV \_ INFO-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) unterstützt. Die -Methode speichert einen Zeiger auf die **IEnumWIA \_ DEV \_ INFO-Schnittstelle** im *Parameter ppIEnum*. Anwendungen können den **IEnumWIA \_ DEV INFO-Schnittstellenzeiger \_** verwenden, um die Eigenschaften jedes WIA 2.0-Geräts aufzählen, das an den Computer des Benutzers angefügt ist.

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenze0er aufrufen, die sie über *den ppIEnum-Parameter* empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
