---
description: Installiert die angegebenen Systemkomponenten.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 7708dd065c066ce3e9fd8e4de1044c6bc8587d2526abdf9aeac175b4387dec42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827244"
---
# <a name="icfginstallinetcomponents-function"></a>IcfgInstallInetComponents-Funktion

Installiert die angegebenen Systemkomponenten.

## <a name="syntax"></a>Syntax


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* 
</dt> <dd>

Ein Handle für das übergeordnete Fenster.

</dd> <dt>

*dwfOptions* 
</dt> <dd>

Eine Kombination der folgenden Flags, die die Installation und Konfiguration steuern.



| Wert                                                                                                                                                                                                                                  | Bedeutung                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ INSTALLMAIL-0x00000004**</dt> <dt></dt> </dl> | Installieren Exchange und Internet-E-Mail.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS-0x00000002**</dt> <dt></dt> </dl>    | Installieren Sie RAS (falls erforderlich).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP-0x00000001**</dt> <dt></dt> </dl>    | Installieren Sie TCP/IP (falls erforderlich).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

Wenn dieser Wert nicht NULL **ist,** ist er bei der Rückgabe nur **true,** wenn Windows neu gestartet werden müssen, um die Installation abzuschließen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Wenn keine Fehler auftreten, wird der **ERROR \_ SUCCESS-Code** zurückgegeben.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
