---
description: Fügt einer Tabelle eine Zeichenfolge und zusätzliche Daten hinzu.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: psetupstringtableaddstringex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358326"
---
# <a name="psetupstringtableaddstringex-function"></a>psetupstringtableaddstringex-Funktion

\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]

Fügt einer Tabelle eine Zeichenfolge und zusätzliche Daten hinzu.

## <a name="syntax"></a>Syntax


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*STRINGTABLE* \[ in\]
</dt> <dd>

Ein Zeiger auf die Zeichen folgen Tabelle.

</dd> <dt>

*Zeichenfolge* \[ in\]
</dt> <dd>

Ein Zeiger auf die Zeichenfolge, die der Tabelle hinzugefügt werden soll.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Der Wert dieses Parameters kann sein `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .



| Wert                                                                                                                                                                                                                                             | Bedeutung                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> "Strauch" <dt>**\_ Mit \_**</dt> Beachtung der Groß-/Kleinschreibung <dt></dt> </dl> | Bei der Zeichenfolge wird die groß-<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> "Strauch" <dt>**\_ Neue \_ ExtraData**</dt> <dt>0x004</dt> </dl>    | Es sind zusätzliche Daten vorhanden.<br/>      |



 

</dd> <dt>

*ExtraData* \[ in, optional\]
</dt> <dd>

Ein optionaler Zeiger auf ein zusätzliches Datenobjekt.

</dd> <dt>

*Extradatasize* \[ in, optional\]
</dt> <dd>

Die Größe der zusätzlichen Daten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
