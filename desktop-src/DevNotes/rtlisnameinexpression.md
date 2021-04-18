---
description: Bestimmt, ob eine Unicode-Zeichenfolge mit dem angegebenen Muster übereinstimmt.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: Rtlisnamenexpression-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340111"
---
# <a name="rtlisnameinexpression-function"></a>Rtlisnamenexpression-Funktion

Bestimmt, ob eine Unicode-Zeichenfolge mit dem angegebenen Muster übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ausdruck* \[ in\]
</dt> <dd>

Ein Zeiger auf die Muster Zeichenfolge. Diese Zeichenfolge kann Platzhalter Zeichen enthalten. Wenn der *ignoreCase* -Parameter den Wert true hat, muss die Zeichenfolge nur Großbuchstaben enthalten.

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

Ein Zeiger auf die Zeichenfolge, die mit dem Muster verglichen werden soll. Diese Zeichenfolge darf keine Platzhalter Zeichen enthalten.

</dd> <dt>

*IgnoreCase* \[ in\]
</dt> <dd>

**True** **, wenn die** Groß-/Kleinschreibung nicht beachtet wird

</dd> <dt>

*Upcasetable* \[ in, optional\]
</dt> <dd>

Ein optionaler Zeiger auf eine Zeichentabelle mit Großbuchstaben, die bei Übereinstimmungen ohne Berücksichtigung der Groß-/Kleinschreibung Wenn dieser Parameter NULL ist, wird die standardmäßige System-Großbuchstaben-Zeichentabelle verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Zeichenfolge mit dem Muster übereinstimmt. Wenn die Zeichenfolge nicht mit dem Muster identisch ist, gibt diese Funktion **false** zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Header Datei zugeordnet. Die zugehörige Import Bibliothek ntdll. lib ist im Microsoft Windows-Treiberkit (WDK) verfügbar. Sie können diese Funktion auch aufrufen, indem Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um eine dynamische Verknüpfung mit Ntdll.dll

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                              |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
