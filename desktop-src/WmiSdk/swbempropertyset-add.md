---
description: Die Add-Methode des-Objekts von "Swap PropertySet" fügt der Auflistung von "gobempropertyset" ein "taubemproperty"-Objekt hinzu. Wenn eine Eigenschaft mit demselben Namen bereits in der Auflistung vorhanden ist, wird der Inhalt durch die neue Definition ersetzt.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Methode "gobempropertyset. Add" (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369041"
---
# <a name="swbempropertysetadd-method"></a>Taubempropertyset. Add-Methode

Die **Add** -Methode des-Objekts von " [**Swap PropertySet**](swbempropertyset.md) " fügt der Auflistung von " **gobempropertyset** " ein " [**taubemproperty**](swbemproperty.md) "-Objekt hinzu. Wenn eine Eigenschaft mit demselben Namen bereits in der Auflistung vorhanden ist, wird der Inhalt durch die neue Definition ersetzt.

> [!Note]  
> Der Wert der hinzugefügten Eigenschaft ist nach diesem Vorgang **null** (nicht zugewiesen). Um den Wert einer WMI-Eigenschaft festzulegen oder zu ändern, müssen Sie die [**value**](swbemdatetime-value.md) -Eigenschaft des zurückgegebenen " [**taubemproperty**](swbemproperty.md) "-Objekts festlegen.

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name der neuen Eigenschaft.

</dd> <dt>

*icimtype* \[ in\]
</dt> <dd>

Erforderlich. Eine ganze Zahl, die den **CimType-Qualifizierer** der neuen Eigenschaft darstellt. Die Liste mit den **CimType-Qualifizierern** und deren Werten finden Sie unter [**wbemcimtypeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) .

</dd> <dt>

*bisarray* \[ in, optional\]
</dt> <dd>

Gibt an, ob die Eigenschaft ein Arraytyp ist. Der Standardwert für diesen Parameter ist **false**.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss NULL sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese Methode ein-Objekt zurück, das die neue [**-Eigenschaft darstellt**](swbemproperty.md) . Andernfalls wird ein **null** -Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Add** -Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Nicht spezifizierter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher für die Ausführung dieser Methode.

</dd> <dt>

**wbemErrInvalidPropertyType** -2147749930
</dt> <dd>

Der **CimType-Qualifizierer** wird nicht erkannt.

</dd> </dl>

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

[**' Swap PropertySet. Remove '**](swbempropertyset-remove.md)
</dt> <dt>

[**Swap Property. Value**](swbemproperty-value.md)
</dt> </dl>

 

 




