---
description: Ruft grundlegende Attribute für das angegebene Datei Objekt ab.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Ntqueryattributesfile-Funktion
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
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351240"
---
# <a name="ntqueryattributesfile-function"></a>Ntqueryattributesfile-Funktion

\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]

Ruft grundlegende Attribute für das angegebene Datei Objekt ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Objectattributes* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [Objekt \_ Attribut](https://msdn.microsoft.com/library/aa491657.aspx) Struktur, die die Attribute bereitstellt, die für das Datei Objekt verwendet werden sollen.

</dd> <dt>

*Fileinformation* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [Datei \_ grundlegende \_ Informations](https://msdn.microsoft.com/library/aa491634.aspx) Struktur, um die zurückgegebenen Datei Attributinformationen zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den NTSTATUS-oder-Fehlercode zurück.

Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes sind in der Header Datei "NTSTATUS. h" aufgeführt, die im WDK verfügbar ist, und werden in der WDK-Dokumentation beschrieben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Header Datei zugeordnet. Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar. Sie können auch die [**LoadLibrary**](-loadlibrary.md) -Funktion und die [**GetProcAddress**](-getprocaddress-.md) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




