---
description: Die Exportfunktion formatproperties formatiert die Daten, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden. Wenn Sie Daten im Detailbereich anzeigen möchten, müssen Sie die Exportfunktion formatproperties in allen Parser-DLLs implementieren.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Formatproperties-Rückruffunktion (Netmon. h)
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
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346687"
---
# <a name="formatproperties-callback-function"></a>Formatproperties-Rückruffunktion

Die Exportfunktion **formatproperties** formatiert die Daten, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden. Wenn Sie Daten im Detailbereich anzeigen möchten, müssen Sie die Exportfunktion **formatproperties** in allen Parser-DLLs implementieren.

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

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame, der analysiert wird.

</dd> <dt>

*lpframe* \[ in\]
</dt> <dd>

Zeiger auf das erste Byte eines Frames.

</dd> <dt>

*lpprotocol* \[ in\]
</dt> <dd>

Zeiger auf den Anfang der Protokolldaten in einem Frame.

</dd> <dt>

*npropertyinsts* \[ in\]
</dt> <dd>

Anzahl der [propertyinst](propertyinst.md) -Strukturen, die von *lppropinst* bereitgestellt werden.

</dd> <dt>

*lppropinst* \[ in\]
</dt> <dd>

Zeiger auf ein Array von [propertyinst](propertyinst.md) -Strukturen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Netzwerkmonitor Ruft die **formatproperties** -Funktion auf, um Daten im Detailbereich der Netzwerkmonitor-Benutzeroberfläche anzuzeigen. Normalerweise wird **formatproperties** aufgerufen, um die Zusammenfassungs Zeile für ein Protokoll zu formatieren, und dann alle Eigenschaften Instanzen des Protokolls innerhalb eines Frames zu formatieren. Netzwerkmonitor garantiert jedoch nicht, wie oft **formatproperties** für einen bestimmten Parser aufgerufen wird.

Während der Implementierung der **formatproperties** -Funktion ruft der Parser indirekt die [formatpropertyinstance](formatpropertyinstance.md) -Funktion auf, um den generischen Formatierer zu verwenden, den Netzwerkmonitor bereitstellt, oder er kann eine benutzerdefinierte formatiererprozedur aufrufen, die vom Parser definiert wird. Eines der Formatierer muss für jede [propertyinst](propertyinst.md) -Struktur aufgerufen werden, die an die Parser-DLL im *lppropinst* -Parameter übergeben wird.



| Informationen zu                                          | Siehe                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.   | [Parser](parsers.md)                                             |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.          | [Architektur der Parser-DLL](parser-dll-architecture.md)             |
| Zum Implementieren von **formatproperties**  gehört ein Beispiel. | [Implementieren von formatproperties](implementing-formatproperties.md) |
| Gibt an, wie der generische Formatierer verschiedene Datentypen formatiert.  | [Generische formatiererausgabe](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Formatpropertyinstance](formatpropertyinstance.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[Propertyinst](propertyinst.md)
</dt> </dl>

 

 




