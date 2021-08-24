---
title: INapComponentConfig2 InvokeUIFromConfigBlob-Methode (NapCommon.h)
description: Wird nach Bedarf von SYSTEM HEALTH Validators (SHVs) implementiert, um die Konfiguration eines Remotecomputers oder lokalen Computers im Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- InvokeUIFromConfigBlob-Methode NAP
- InvokeUIFromConfigBlob-Methode NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2-Schnittstelle NAP , InvokeUIFromConfigBlob-Methode
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
ms.openlocfilehash: 45d85e0506b8adf084b65a13a117a9dea3856fcff2e73f65a229bdb31b283fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803160"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>INapComponentConfig2::InvokeUIFromConfigBlob-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **InvokeUIFromConfigBlob-Methode** wird nach Bedarf von SYSTEM HEALTH Validators (SHVs) implementiert, um die Konfiguration eines Remotecomputers oder lokalen Computers im Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht. Die Konfigurationskomponente muss die Verwendung von [**INapComponentConfig**](inapcomponentconfig.md) über DCOM unterstützen.

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

*hwndParent* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Oder Besitzerfenster. Ein gültiges Fensterhandle muss angegeben werden.

</dd> <dt>

*inbCount* \[ In\]
</dt> <dd>

Die Größe von *inData in* Bytes.

</dd> <dt>

*inData* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, in dem die anfänglichen Konfigurationsdaten gespeichert werden. Diese Daten werden vom Remotecomputer oder lokalen Computer exportiert.

</dd> <dt>

*outbCount* \[ out\]
</dt> <dd>

Die Größe von *outdata* in Bytes.

</dd> <dt>

*outdata* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Konfigurationsdaten speichert, die von der SHV-Konfigurations-Benutzeroberfläche geändert wurden. Diese Daten werden vom Remotecomputer oder lokalen Computer importiert.

</dd> <dt>

*fConfigChanged* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **BOOL,** die auf **TRUE** festgelegt ist, wenn die Konfiguration während des Ui-Vorgangs geändert wurde, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen der Standardfehlercodes Windows zurück.

## <a name="remarks"></a>Hinweise

Wenn diese Funktion für einen lokalen Computer verwendet wird, kann sie für die SHV-Konfiguration pro Richtlinie verwendet werden. Sie bietet eine Möglichkeit, eine SHV-Benutzeroberfläche aufzurufen und eine vorhandene SHV-Konfiguration zu bearbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





