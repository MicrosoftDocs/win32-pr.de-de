---
description: Die Remove-Methode des Objekts "Swap PropertySet" löscht eine Eigenschaft aus der Sammlung "Swap PropertySet".
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: "' Swap PropertySet. Remove '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130980"
---
# <a name="swbempropertysetremove-method"></a>Methode ' Swap PropertySet. Remove '

Die **Remove** -Methode des Objekts " [**Swap PropertySet**](swbempropertyset.md) " löscht eine Eigenschaft aus der Sammlung " **Swap PropertySet** ".

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name des zu entfernenden Elements.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Wenn angegeben, muss dieser Wert 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Remove** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Nicht spezifizierter Fehler.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

Der Benutzer hat versucht, eine Eigenschaft zu löschen, die nicht gelöscht werden kann.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Die angegebene Eigenschaft ist nicht vorhanden.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher für die Ausführung dieser Methode.

</dd> <dt>

**wbemErrPropagatedProperty** -142927303552 (0x2147219380)
</dt> <dd>

Der Benutzer hat versucht, eine Eigenschaft zu löschen, deren Besitzer er nicht war. Die Eigenschaft wurde von einer übergeordneten Klasse vererbt.

</dd> <dt>

**wbemErrResetToDefault** -2147758082 (0x80043002)
</dt> <dd>

Der Benutzer löschte einen Außerkraftsetzungs Standardwert für die aktuelle Klasse. Der Standardwert für diese Eigenschaft in der übergeordneten Klasse wurde reaktiviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eigenschaften können nicht aus Klassen Instanzen oder abgeleiteten Klassen mit geerbten Eigenschaften entfernt werden. Bei solchen löschversuchen wird ein Fehler ausgegeben, und die-Eigenschaft wird nicht entfernt. die-Eigenschaft wird auf ihren Standardwert zurückgesetzt.

Beim Entfernen von Elementen ist es nicht möglich, eine Auflistung zu durchlaufen, denn wenn Sie ein Element aus einer Auflistung entfernen, wird der Auflistungs Zeiger zum nächsten Element verschoben. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

## <a name="examples"></a>Beispiele

Ein Codebeispiel, in dem diese Methode verwendet wird, finden Sie im Thema zu " [**Swap-PropertySet**](swbempropertyset.md) ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Eigenschaften Satz<br/>                                                      |
| IID<br/>                      | IID \_ iswbempropertyset<br/>                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap PropertySet**](swbempropertyset.md)
</dt> <dt>

[**Austauschen von "Swap PropertySet. Add"**](swbempropertyset-add.md)
</dt> </dl>

 

 




