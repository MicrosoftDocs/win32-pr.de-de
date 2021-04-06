---
title: INapComponentConfig2 invokeuifromconfigblob-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) nach Bedarf implementiert, um die Konfiguration eines Remote Computers oder eines lokalen Computers in den Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Invokeuifromconfigblob-Methode NAP
- Invokeuifromconfigblob-Methode NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2 Interface NAP, invokeuifromconfigblob-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858777"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>INapComponentConfig2:: invokeuifromconfigblob-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **invokeuifromconfigblob** -Methode wird nach Bedarf von System Integritätsprüfungen (SHVs) implementiert, um die Konfiguration eines Remote Computers oder eines lokalen Computers in den Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht. Die Konfigurationskomponente muss die Verwendung von [**inapcomponentconfig**](inapcomponentconfig.md) über DCOM unterstützen.

## <a name="syntax"></a>Syntax


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster oder Besitzer Fenster. Ein gültiges Fenster Handle muss angegeben werden.

</dd> <dt>

*inbcount* \[ in\]
</dt> <dd>

Die Größe von *InData* in Byte.

</dd> <dt>

*InData* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, in dem die anfänglichen Konfigurationsdaten gespeichert werden. Diese Daten werden vom Remote-oder lokalen Computer exportiert.

</dd> <dt>

*outbcount* \[ vorgenommen\]
</dt> <dd>

Die Größe (in Bytes) der *OutData*.

</dd> <dt>

*OutData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, in dem Konfigurationsdaten gespeichert werden, die von der SHV-Konfigurations Benutzeroberfläche geändert wurden. Diese Daten werden vom Remote-oder lokalen Computer importiert.

</dd> <dt>

nicht *geändert* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **booleschen** Wert, der auf **true** festgelegt ist, wenn die Konfiguration während des UI-Vorgangs geändert wurde, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen der standardmäßigen Windows-Fehlercodes zurück.

## <a name="remarks"></a>Bemerkungen

Bei Verwendung für einen lokalen Computer kann diese Funktion für die SHV-Konfiguration pro Richtlinie verwendet werden. Es bietet eine Möglichkeit, eine SHV-Benutzeroberfläche aufzurufen und eine vorhandene SHV-Konfiguration zu bearbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





