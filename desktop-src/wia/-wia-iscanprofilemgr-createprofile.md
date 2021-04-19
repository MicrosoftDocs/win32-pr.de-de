---
description: Erstellt ein leeres Überprüfungs Profil und ordnet es einem Scanner oder einem anderen Windows-Abbild Erfassungs Element (WIA) 2,0 zu.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Iscanprofilemgr:: kreateprofile-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485294"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>Iscanprofilemgr:: kreateprofile-Methode

Erstellt ein leeres Überprüfungs Profil und ordnet es einem Scanner oder einem anderen Windows-Abbild Erfassungs Element (WIA) 2,0 zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die ID des Geräts oder des WIA-2,0-Elements.

</dd> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Der Anzeige Name des neuen Profils.

</dd> <dt>

*guidcategory* \[ in\]
</dt> <dd>

Typ: **GUID**

Der GUID der Kategorie des Geräts oder eines WIA-2,0-Elements. Dabei muss es sich um eine der WIA- \_ IPA- \_ Element Kategorie- \_ Konstanten handeln.

</dd> <dt>

*ppscanprofile* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***

Die Adresse eines Zeigers auf das neue Profil.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**Iscanprofilemgr:: kreateprofile** ordnet das angegebene Gerät dem neuen Überprüfungs Profil zu.

**Iscanprofilemgr:: kreateprofile** generiert automatisch eine GUID für das neue Profil. Holen Sie sich die GUID mit [**GetGuid**](-wia-iscanprofile-getguid.md).

Verwenden Sie die [**iscanprofilemgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) -Methode, wenn mehrere [**iscanprofilemgr**](-wia-iscanprofilemgr.md) -Objekte gleichzeitig Profile erstellen oder löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofilemgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




