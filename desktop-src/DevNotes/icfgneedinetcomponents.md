---
description: Bestimmt, ob in den Optionen markierte Komponenten auf dem System installiert sind.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Icsgneedinetcomponents-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362038"
---
# <a name="icfgneedinetcomponents-function"></a>Icsgneedinetcomponents-Funktion

Bestimmt, ob in den Optionen markierte Komponenten auf dem System installiert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DWF Options* 
</dt> <dd>

Eine Kombination der folgenden Flags, die angeben, welche Komponenten in der folgenden Liste erkannt werden sollen.



| Wert                                                                                                                                                                                                                                  | Bedeutung                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ Installmail**</dt> <dt>0x00000004</dt> </dl> | Ist Exchange oder Internet-e-Mail erforderlich?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ Installras**</dt> <dt>0x00000002</dt> </dl>    | Ist RAS erforderlich?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ Installtcp**</dt> <dt>0x00000001</dt> </dl>    | Ist TCP/IP erforderlich?<br/>                    |



 

</dd> <dt>

*lpfneedcomponents* 
</dt> <dd>

Wenn dieser Wert nicht **null** ist, ist es bei der Rückgabe **true** , wenn mindestens eine Komponente nicht auf dem System installiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Wenn keine Fehler auftreten, wird der **Fehler \_ Erfolgs** Code zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
