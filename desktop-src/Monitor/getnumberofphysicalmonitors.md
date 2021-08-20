---
title: GetNumberOfPhysicalMonitors-Funktion
description: Ruft die Anzahl der einem Anzeigegerät zugeordneten physischen Monitore ab.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- GetNumberOfPhysicalMonitors-Funktion Monitorkonfiguration
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673ef12d1e02d87e068784408824bb78dbbbad5dfd5c907ece58c3eb7673e957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534930"
---
# <a name="getnumberofphysicalmonitors-function"></a>GetNumberOfPhysicalMonitors-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Überwachungskonfigurations-API verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Ruft die Anzahl der einem Anzeigegerät zugeordneten physischen Monitore ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrDeviceName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**UNICODE \_ STRING-Struktur,**](/windows/desktop/api/subauth/ns-subauth-unicode_string) die den Namen des Anzeigegeräts enthält, wie von der [**GetMonitorInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) zurückgegeben.

</dd> <dt>

*pdwNumberOfPhysicalMonitors* \[ out\]
</dt> <dd>

Empfängt die Anzahl der physischen Monitore.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufrufen:

-   [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

Dieser Funktion ist keine Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Überwachen von Konfigurationsfunktionen](monitor-configuration-functions.md)
</dt> </dl>

 

