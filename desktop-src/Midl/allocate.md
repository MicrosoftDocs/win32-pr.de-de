---
title: allocate-Attribut
description: Mit dem Attribut \allocate\ ACF können Sie die Speicherzuordnung und -freigabe für einen in der IDL-Datei definierten Typ anpassen.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- ATTRIBUT MIDL zuordnen
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345652b9da5ed5087793606d963d6cf9b8ce225587ee150c27f6410ae99b8d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808440"
---
# <a name="allocate-attribute"></a>allocate-Attribut

Mit **\[ dem Attribut \] "ACF** zuordnen" können Sie die Speicherzuordnung und -freigabe für einen in der IDL-Datei definierten Typ anpassen.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*allocate-option-list* 
</dt> <dd>

Gibt eine oder mehrere Speicherbelegungsoptionen an. Wählen Sie entweder einen **einzelnen \_ Knoten oder** alle **\_ Knoten** aus, oder wählen Sie entweder einen von **free** oder **don't \_ free** oder einen aus jedem Paar aus. Wenn Sie mehrere Optionen angeben, trennen Sie die Optionen durch Kommas.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt andere optionale ACF-Typattribute an. Wenn Sie mehrere Typattribute angeben, trennen Sie die Optionen durch Kommas.

</dd> <dt>

*type-name* 
</dt> <dd>

Gibt einen in der IDL-Datei definierten Typ an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ Attribut allocate \]** verfügt über die folgenden gültigen Optionen.



| Option           | BESCHREIBUNG                                                           |
|------------------|-----------------------------------------------------------------------|
| **Alle \_ Knoten**   | Es wird ein Aufruf zum Zuordnen und Zum Freien von Arbeitsspeicher für alle Knoten verwendet.             |
| **Einzelner \_ Knoten** | Es werden viele einzelne Aufrufe ausgeführt, um jedem Knoten Arbeitsspeicher zu reservieren und frei zu geben. |
| **free**         | Gibt Arbeitsspeicher bei Rückgabe aus dem Serverstub frei.                          |
| **nicht \_ kostenlos**   | Gibt bei Rückgabe aus dem Serverstub keinen Arbeitsspeicher frei.                  |



 

Standardmäßig können die Stubs Speicher für Daten zuordnen, auf die von einem eindeutigen oder vollständigen Zeiger verwiesen wird, indem [**midl \_ user \_ allocate**](midl-user-allocate-1.md) und [**midl \_ user \_ free**](midl-user-free-1.md) einzeln für jeden Zeiger aufruft.

Sie können die Geschwindigkeit Ihrer Anwendung optimieren, indem Sie die Option alle **Knoten \_ angeben.** Diese Option weist den Stub an, die Größe des ganzen Arbeitsspeichers zu berechnen, auf den über den Zeiger des angegebenen Typs verwiesen wird, und einen einzelnen Aufruf von midl zu [**\_ \_**](midl-user-allocate-1.md)verwenden. Der Stub gibt den Arbeitsspeicher frei, indem ein Aufruf von [**midl \_ user free (Midl-Benutzer \_ frei) aufruft.**](midl-user-free-1.md)

Die **Option Nicht frei \_ leitet** den MIDL-Compiler an, einen Serverstub zu generieren, der [**midl user \_ \_ free**](midl-user-free-1.md) für den angegebenen Typ nicht aufruft. Die **Option Nicht frei \_ ermöglicht** es, dass die Zeigerstrukturen für die Serveranwendung zugänglich bleiben, nachdem der Remoteprozeduraufruf abgeschlossen und an den Client zurückgegeben wurde.

Das **\[ Attribut allocate \]** führt dazu, dass jeder **\[ \] in-out-Parameter,** der ein Zeiger auf einen Typ ist, der mit der Option "Alle Knoten" qualifiziert ist, Speicher neu zuteilen, wenn die Daten nicht gespeichert werden. **\_** Es liegt in der Verantwortung der Anwendung, den zuvor für diesen Parameter zugeordneten Arbeitsspeicher frei zu geben. Beispiel:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

Der PTHISTYPE-Datentyp wird vom Stub [**\[ \]**](out-idl.md) vor dem Unmarshaling in Out-Richtung neu zugewiesen. Aus diesem Grund muss die Anwendung den Arbeitsspeicher, den sie zuvor für die Daten dieses Parameters zugeordnet hat, frei geben, da ein Arbeitsspeicherverlust auftritt.

## <a name="examples"></a>Beispiele

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**In**](in.md)
</dt> <dt>

[**midl \_ user \_ allocate**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




