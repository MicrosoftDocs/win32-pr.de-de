---
description: Ruft grundlegende Attribute für das angegebene Dateiobjekt ab.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: e6b1ecdc7cc7f0a5c18afc3eeb613c3f9cd9a38aa22a876ad156c3d1c6b1bc97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826806"
---
# <a name="ntqueryattributesfile-function"></a>NtQueryAttributesFile-Funktion

\[Diese Funktion kann ohne weitere Ankündigung geändert oder Windows entfernt werden.\]

Ruft grundlegende Attribute für das angegebene Dateiobjekt ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ObjectAttributes* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [OBJECT \_ ATTRIBUTES-Struktur,](https://msdn.microsoft.com/library/aa491657.aspx) die die Für das Dateiobjekt zu verwendenden Attribute liefert.

</dd> <dt>

*FileInformation* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [FILE \_ BASIC \_ INFORMATION-Struktur,](https://msdn.microsoft.com/library/aa491634.aspx) um die zurückgegebenen Dateiattributinformationen zu empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen NTSTATUS- oder Fehlercode zurück.

Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes sind in der im WDK verfügbaren Ntstatus.h-Headerdatei aufgeführt und in der WDK-Dokumentation beschrieben.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Headerdatei zugeordnet. Die zugeordnete Importbibliothek Ntdll.lib ist im WDK verfügbar. Sie können auch die [**Funktionen LoadLibrary**](-loadlibrary.md) und [**GetProcAddress**](-getprocaddress-.md) verwenden, um dynamisch eine Verknüpfung mit Ntdll.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




