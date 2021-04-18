---
description: Die attachpropertyinstanceex-Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu und ändert den Wert der Eigenschafts Daten.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Attachpropertyinstanceex-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358428"
---
# <a name="attachpropertyinstanceex-function"></a>Attachpropertyinstanceex-Funktion

Die **attachpropertyinstanceex** -Funktion ordnet eine vorhandene Eigenschaft einer bestimmten Position in den erkannten Daten zu und ändert den Wert der Eigenschafts Daten.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame, der analysiert wird. Verwenden Sie das Handle, das an die Parser-DLL im *hframe* -Parameter der [**attachproperties**](attachproperties.md) -Funktion übergeben wird.

</dd> <dt>

*hproperty* \[ in\]
</dt> <dd>

Handle für eine [**PropertyInfo**](propertyinfo.md) -Struktur, die die Eigenschaft definiert. Beim Implementieren der [**Register**](register-parser.md) Export-Funktion geben Sie die **PropertyInfo** -Struktur an, die die Eigenschaft definiert.

</dd> <dt>

*Länge* \[ in\]
</dt> <dd>

Länge der Daten für diese Instanz der-Eigenschaft.

</dd> <dt>

*lpdata* \[ in\]
</dt> <dd>

Ein Zeiger auf die Position in den erkannten Daten, in der sich der Eigenschafts Wert befindet. Verwenden Sie den Zeiger, der an die Parser-DLL im *lpprotocol* -Parameter der [**attachproperties**](attachproperties.md) -Funktion übergeben wird.

</dd> <dt>

*Verlängert* \[ in\]
</dt> <dd>

Länge der erweiterten Daten Länge in Bytes.

</dd> <dt>

*lpdataex* \[ in\]
</dt> <dd>

Zeiger auf die erweiterten Daten, bei dem es sich in der Regel um eine Stapel Variable handelt, die die erweiterten Daten enthält.

</dd> <dt>

*HelpID* \[ in\]
</dt> <dd>

Bezeichner (von 0 bis 2047), der verwendet wird, um die kontextbezogene Hilfe für eine Eigenschaft festzulegen.

Die *HelpID* -Nummer ist relativ zur Hilfedatei, die der Protokoll [*Eigenschaften Datenbank*](p.md)zugeordnet ist.

</dd> <dt>

*Einzug* \[ in\]
</dt> <dd>

Einzugs Ebene (von 0 bis 15) wird verwendet, um eine Eigenschaft hierarchisch anzuzeigen.

Netzwerkmonitor verwendet die Ebenen 0 bis 9. Ebene 15 ist ein spezieller Wert, der es dem Parser ermöglicht, eine verborgene Eigenschaft anzufügen, die nicht sichtbar ist.

</dd> <dt>

*IFlags* \[ in\]
</dt> <dd>

Ein bitfeldwert, der die Reihenfolge der Bits innerhalb einer Eigenschaft angibt. Vorherige Parser, die *ferror* auf 0 oder 1 festgelegt haben, sollten nun *ferror* auf den iflag- \_ Fehler festlegen. Legen Sie diesen Parameter auf einen der folgenden Werte fest.



| Wert                                                                                                                                                         | Bedeutung                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**iflag- \_ Fehler**</dt> </dl>       | Die Daten im Frame weisen einen Fehler auf.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**iflag wurde \_ ausgetauscht**</dt> </dl> | Zum Anfüge Zeitpunkt ist **Word** Byte ein nicht-Intel-Format.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**iflag- \_ Unicode**</dt> </dl> | Zum Anfüge Zeitpunkt ist die **Zeichenfolge** Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Die " **attachpropertyinstanceex** "-Funktion wird während der Implementierung der " [**attachproperties**](attachproperties.md) "-Exportfunktion aufgerufen. Wenn eine Eigenschaft mithilfe von attachpropertyinstanceex an die Daten angefügt wird, erstellt Netzwerkmonitor eine [**propertyinst**](propertyinst.md) -Struktur, die die Instanz der angefügten Eigenschaft definiert, und eine [**propertyinstex**](propertyinstex.md) -Struktur, die die erweiterten Daten definiert.

Wenn " **attachpropertyinstanceex** " aufgerufen wird und keine erweiterten Daten bereitgestellt werden, ist der *lpdataex* -Parameter **null** , oder der Parameter " *verlänex* " ist 0, der **attachpropertyinstanceex** -Aufruf ist funktional äquivalent zu einem [**attachpropertyinstance**](attachpropertyinstance.md) -Aufruf.

Bei der Implementierung von [**attachproperties**](attachproperties.md)wird [**attachpropertyinstance**](attachpropertyinstance.md) aufgerufen, um die Daten zu verwenden, wie Sie in der Erfassung vorhanden sind. Sie können auch die **attachpropertyinstanceex** -Funktion aufrufen, um die Eigenschaften Daten zu ändern. Es wird jedoch empfohlen, dass Sie die Daten verwenden, wie Sie in der Erfassung vorhanden sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




