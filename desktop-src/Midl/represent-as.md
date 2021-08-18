---
title: represent_as-Attribut
description: Das Attribut \represent as\ ACF ordnet einen benannten lokalen Typ im Repr-Typ der Zielsprache einem Übertragungstyp namens -type zu, der zwischen Client und \_ Server übertragen wird.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as MIDL-Attribut
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c76576a7d6710c54573ff78186b3cf6d347afc8c4c242fd6e4c1d49865fb521f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146363"
---
# <a name="represent_as-attribute"></a>als \_ Attribut darstellen

Das **\[ als \_ \]** ACF-Attribut darstellen ordnet einen benannten lokalen Typ im *Repr-Typ* der Zielsprache einem Übertragungstyp namens *type* zu, der zwischen Client und Server übertragen wird.

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*named-type* 
</dt> <dd>

Gibt den benannten Übertragungsdatentyp an, der zwischen Client und Server übertragen wird.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die für den Typ gelten. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*repr-type* 
</dt> <dd>

Gibt den dargestellten lokalen Typ in der Zielsprache an, der den Client- und Serveranwendungen präsentiert wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie **\[ als \_ \] verwenden,** müssen Sie Routinen zur Konvertierung zwischen dem lokalen und dem Übertragungstypen sowie den freien Arbeitsspeicher, der zum Halten der konvertierten Daten verwendet wird, zur Verfügung stellen. Das **\[ Attribut represent \_ as \]** weist die Stubs an, die vom Benutzer bereitgestellten Konvertierungsroutinen auf aufruft.

Der übertragene Typ *named-type* muss in einen MIDL-Basistyp, vordefinierten Typ oder in einen Typbezeichner auflösen. Weitere Informationen finden Sie unter [MIDL-Basistypen.](midl-base-types.md)

Sie müssen die folgenden Routinen liefern:



| Routinename                   | Beschreibung                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *named \_ type** \_ aus dem \_ lokalen** | Konvertiert Daten vom lokalen Typ in den Netzwerktyp. Die Routine ordnet Arbeitsspeicher für den Netzwerkdatentyp zu, einschließlich Arbeitsspeicher für alle Daten, auf die von Zeigern im Netzwerkdatentyp verwiesen wird.              |
| *named \_ type** \_ in \_ local**   | Konvertiert Daten vom Netzwerktyp in den lokalen Typ. Die Routine ist für die Zuweisung von Arbeitsspeicher für Daten zuständig, auf die von Zeigern im lokalen Typ verwiesen wird. RPC weist Arbeitsspeicher für den lokalen Typ selbst zu. |
| *named \_ type** \_ free \_ local** | Gibt Arbeitsspeicher frei, der für Daten zugeordnet ist, auf die von Zeigern im lokalen Typ verwiesen wird. RPC gibt Arbeitsspeicher für den Typ selbst frei                                                                                             |
| *named \_ type** \_ free \_ inst**  | Gibt Arbeitsspeicher frei, der für die Daten, auf die von Zeigern im Netzwerktyp verwiesen wird, und für den Netzwerktyp selbst reserviert ist.                                                                                            |



 

Der Clientstub ruft *named-type** aus \_ \_ local** auf, um Speicherplatz für den übertragenen Typ zu reservieren und die Daten vom lokalen Typ in den Netzwerktyp zu übersetzen. Der Serverstub weist Speicherplatz für den ursprünglichen Datentyp zu und ruft *named-type** auf \_ \_ local** auf, um die Daten vom Netzwerktyp in den lokalen Typ zu übersetzen.

Nach der Rückgabe aus dem Anwendungscode rufen die Client- und Serverstubs *named-type** \_ free \_ inst** auf, um die Speicherbelegung für den Netzwerktyp frei zu machen. Der Clientstub ruft *named-type** \_ free \_ local** auf, um die Von der Routine zurückgegebene Speicher frei zu machen.

Die folgenden Typen können kein -Attribut **\[ als \_ \] -Attribut** darstellen:

-   Konforme, unterschiedliche oder konforme unterschiedliche Arrays
-   Strukturen, in denen der letzte Member ein konformes Array ist (eine konforme Struktur)
-   Zeiger oder Typen, die einen Zeiger enthalten
-   Pipes oder Typen, die Pipes enthalten
-   Typen, die als Basistyp für eine Pipe verwendet werden
-   Vordefinierte Typen verarbeiten [**\_ t**](handle-t.md), [**void**](void.md)
-   Typen mit dem [**\[ Handleattribut \]**](handle.md)

## <a name="examples"></a>Beispiele

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




