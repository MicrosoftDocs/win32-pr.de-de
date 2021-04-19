---
description: Formatiert die eigenschafteninstanzdaten mit dem von Netzwerkmonitor bereitgestellten generischen Formatierer.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Formatpropertyinstance-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346276"
---
# <a name="formatpropertyinstance-function"></a>Formatpropertyinstance-Funktion

Die Funktion **formatpropertyinstance** formatiert die eigenschafteninstanzdaten mit dem generischen Formatierer, den Netzwerkmonitor bereitstellt.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lppropertyinst* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [propertyinst](propertyinst.md) -Struktur, die die Instanzdaten enthält.

Bei der Eingabe nimmt das generische Formatierungs Programm die Instanzdaten von einem der **propertyinst** -Union-Member an und konvertiert diese Daten in eine vordefinierte formatierte Zeichenfolge.

Bei der Ausgabe legt das generische Formatierer den **szpropertytext** -Member der **propertyinst** -Struktur auf einen Zeiger auf die formatierte Zeichenfolge fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode von "nmerr. h".

## <a name="remarks"></a>Bemerkungen

Die parserdll ruft indirekt die **formatpropertyinstance** -Funktion auf, wenn der generische Formatierer zum Formatieren von Daten für die Anzeige im Detailbereich der Netzwerkmonitor-Benutzeroberfläche erforderlich ist. Um **formatpropertyinstance** aufzurufen, geben Sie diese im **InstanceData** -Member der [PropertyInfo](propertyinfo.md) -Struktur an, wenn Sie die Eigenschaft definieren.

> [!Note]  
> Der Parser erkennt nicht, welche Funktion aufgerufen wird, wenn eine Instanz einer Eigenschaft formatiert werden muss. Bei der Funktion kann es sich um eine **formatpropertyinstance** oder eine vom Parser definierte benutzerdefinierte Format Funktion handeln. Der Parser Ruft eine beliebige Format Funktion auf, die vom **InstanceData** -Member der **PropertyInfo** -Struktur für die Eigenschaft angegeben wird.

 

Weitere Informationen und ein Beispiel für die Implementierung von [formatproperties](formatproperties.md)finden Sie unter [Implementieren von formatproperties](implementing-formatproperties.md). Weitere Informationen dazu, wie das generische Formatierungssystem verschiedene Datentypen formatiert, finden Sie unter [generische formatiererausgabe](generic-formatter-output.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[Propertyinst](propertyinst.md)
</dt> </dl>

 

 




