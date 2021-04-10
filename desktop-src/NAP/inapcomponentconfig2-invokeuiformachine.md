---
title: INapComponentConfig2 invokeuiformachine-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) nach Bedarf implementiert, um die Remote Konfiguration direkt auf dem angegebenen Computer zu verwalten. Mit dieser Methode wird eine Benutzeroberfläche der Konfigurations Verwaltung gestartet.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Invokeuiformachine-Methode NAP
- Invokeuiformachine-Methode NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2 Interface NAP, invokeuiformachine-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103539"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>INapComponentConfig2:: invokeuiformachine-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **invokeuiformachine** -Methode wird von System Integritätsprüfungen (SHVs) nach Bedarf implementiert, um die Remote Konfiguration direkt auf dem angegebenen Computer zu verwalten. Mit dieser Methode wird eine Benutzeroberfläche der Konfigurations Verwaltung gestartet.

## <a name="syntax"></a>Syntax


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster oder Besitzer Fenster. Ein gültiges Fenster Handle muss angegeben werden.

</dd> <dt>

*MachineName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**zählzeichenfolge**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , die den Computernamen des NAP-Clients enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen der standardmäßigen Windows-Fehlercodes zurück.

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

 

 





