---
description: Installiert die angegebenen Systemkomponenten.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Icsginstallinetcomponents-Funktion
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
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352968"
---
# <a name="icfginstallinetcomponents-function"></a>Icsginstallinetcomponents-Funktion

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

*DWF Options* 
</dt> <dd>

Eine Kombination der folgenden Flags, die die Installation und Konfiguration steuern.



| Wert                                                                                                                                                                                                                                  | Bedeutung                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ Installmail**</dt> <dt>0x00000004</dt> </dl> | Installieren Sie Exchange und Internet-e-Mail.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ Installras**</dt> <dt>0x00000002</dt> </dl>    | Installieren Sie RAS (falls erforderlich).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ Installtcp**</dt> <dt>0x00000001</dt> </dl>    | Installieren Sie TCP/IP (falls erforderlich).<br/>         |



 

</dd> <dt>

*lpfneedsrestart* 
</dt> <dd>

Wenn dieser Wert ungleich **null** ist, wird bei der Rückgabe nur dann **true** angezeigt, wenn Windows neu gestartet werden muss, um die Installation abzuschließen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Wenn keine Fehler auftreten, wird der **Fehler \_ Erfolgs** Code zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
