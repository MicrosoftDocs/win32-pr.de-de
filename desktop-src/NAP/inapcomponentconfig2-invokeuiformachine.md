---
title: INapComponentConfig2 InvokeUIForMachine-Methode (NapCommon.h)
description: Wird nach Bedarf von SYSTEM HEALTH Validators (SHVs) implementiert, um die Remotekonfiguration direkt auf dem angegebenen Computer zu verwalten. Diese Methode startet eine Benutzeroberfläche für die Konfigurationsverwaltung.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- InvokeUIForMachine-Methode NAP
- InvokeUIForMachine-Methode NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2-Schnittstelle NAP , InvokeUIForMachine-Methode
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
ms.openlocfilehash: 8321425cf878bd9b3d8702f73fa464ae069420cd0e59f57e2500151fda01b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940188"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>INapComponentConfig2::InvokeUIForMachine-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **InvokeUIForMachine-Methode** wird nach Bedarf von SYSTEM HEALTH Validators (SHVs) implementiert, um die Remotekonfiguration direkt auf dem angegebenen Computer zu verwalten. Diese Methode startet eine Benutzeroberfläche für die Konfigurationsverwaltung.

## <a name="syntax"></a>Syntax


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Oder Besitzerfenster. Ein gültiges Fensterhandle muss angegeben werden.

</dd> <dt>

*machineName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CountedString,**](/windows/win32/api/naptypes/ns-naptypes-countedstring) die den Computernamen des NAP-Clients enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen der Standardfehlercodes Windows zurück.

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

 

 





