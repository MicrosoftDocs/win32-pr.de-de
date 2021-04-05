---
description: Erstellt einen Enumerator mit Eigenschafts Informationen für jedes verfügbare Windows-Abbild Erfassungsgerät (WIA) 2,0.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2:: enumdevicumfo-Methode (WIA. h)'
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
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752840"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>IWiaDevMgr2:: enumdevicumfo-Methode

Erstellt einen Enumerator mit Eigenschafts Informationen für jedes verfügbare Windows-Abbild Erfassungsgerät (WIA) 2,0.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt den Typ der aufzuzählenden WIA 2,0-Geräte an.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA-Aufzählung ( \_ \_ \_ lokal)**


</dt> <dd>

Nur lokal verbundene aktive Überprüfungs Geräte werden aufgezählt.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA-Aufzählung \_ \_ \_ alle**


</dt> <dd>

Alle Geräte werden sowohl lokal als auch Remote aufgelistet, einschließlich inaktiver (nicht verbundener) Geräte und Legacy-Geräte mit nur-STI-Geräten.

</dd> </dl> </dd> <dt>

*ppiumum* \[ Out, retval\]
</dt> <dd>

Typ: **[ **ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Empfängt die Adresse eines Zeigers auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die **IWiaDevMgr2:: enumdeviceinfo** -Methode erstellt ein Enumeratorobjekt, das die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle unterstützt. Die-Methode speichert einen Zeiger auf die **ienumwia \_ dev \_ Info** -Schnittstelle im Parameter *ppienumum*. Anwendungen können den **ienumwia \_ dev \_ Info** -Schnittstellen Zeiger verwenden, um die Eigenschaften jedes WIA 2,0-Geräts aufzulisten, das mit dem Computer des Benutzers verbunden ist.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienum* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
