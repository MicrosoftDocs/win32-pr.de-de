---
description: Die Exportfunktion FormatProperties formatiert die Daten, die im Detailbereich der Netzwerkmonitor Ui angezeigt werden. Wenn Sie Daten im Detailbereich anzeigen möchten, müssen Sie die Exportfunktion FormatProperties in allen Parser-DLLs implementieren.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: FormatProperties-Rückruffunktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 6bb0bc74a52569edbb922aa93edd27b53106073ffdafa3a6cacc5808aab71eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012248"
---
# <a name="formatproperties-callback-function"></a>Rückruffunktion "FormatProperties"

Die **Exportfunktion FormatProperties** formatiert die Daten, die im Detailbereich der Netzwerkmonitor Ui angezeigt werden. Wenn Sie Daten im Detailbereich anzeigen möchten, müssen Sie die **Exportfunktion FormatProperties** in allen Parser-DLLs implementieren.

## <a name="syntax"></a>Syntax


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame, der analysiert wird.

</dd> <dt>

*lpFrame* \[ In\]
</dt> <dd>

Zeiger auf das erste Byte eines Frames.

</dd> <dt>

*lpProtocol* \[ In\]
</dt> <dd>

Zeiger auf den Anfang der Protokolldaten in einem Frame.

</dd> <dt>

*nPropertyInsts* \[ In\]
</dt> <dd>

Anzahl der [PROPERTYINST-Strukturen,](propertyinst.md) die von *lpPropInst* bereitgestellt werden.

</dd> <dt>

*lpPropInst* \[ In\]
</dt> <dd>

Zeiger auf ein Array von [PROPERTYINST-Strukturen.](propertyinst.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Netzwerkmonitor ruft die **FormatProperties-Funktion** auf, um Daten im Detailbereich der Netzwerkmonitor-Benutzeroberfläche anzuzeigen. In der Regel wird **FormatProperties** aufgerufen, um die Zusammenfassungszeile für ein Protokoll und dann alle Eigenschafteninstanzen des Protokolls innerhalb eines Frames zu formatieren. Netzwerkmonitor garantiert jedoch nicht, wie oft **FormatProperties** für einen bestimmten Parser aufruft.

Während der Implementierung der **FormatProperties-Funktion** ruft der Parser indirekt die [FormatPropertyInstance-Funktion](formatpropertyinstance.md) auf, um den generischen Formatierer zu verwenden, den Netzwerkmonitor bereitstellt, oder er kann eine benutzerdefinierte Formatierungsprozedur aufrufen, die vom Parser definiert wird. Einer der Formatierer muss für jede [PROPERTYINST-Struktur](propertyinst.md) aufgerufen werden, die im *lpPropInst-Parameter* an die Parser-DLL übergeben wird.



| Informationen zu                                          | Siehe                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor arbeiten.   | [Parser](parsers.md)                                             |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.          | [Parser-DLL-Architektur](parser-dll-architecture.md)             |
| Die Implementierung von **FormatProperties**  umfasst ein Beispiel. | [Implementieren von FormatProperties](implementing-formatproperties.md) |
| Formatieren verschiedener Datentypen durch das generische Formatierungsformatierer  | [Generische Formatierungsausgabe](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[Propertyinfo](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




