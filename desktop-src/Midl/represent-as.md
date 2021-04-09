---
title: represent_as-Attribut
description: Das Attribut \ ist \_ As \ ACF ordnet einen benannten lokalen Typ in der Zielsprache repr-Type mit einem Übertragungstyp namens-Type zu, der zwischen Client und Server übertragen wird.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as Attribut-Mittel l
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037722"
---
# <a name="represent_as-attribute"></a>\_als Attribut darstellen

Das Attribut " **\[ \_ As \]** ACF" wird in der Zielsprache " *repr-Type* " mit einem Übertragungstyp *namens "-Type* " verknüpft, der zwischen Client und Server übertragen wird.

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

*benannter Typ* 
</dt> <dd>

Gibt den benannten Übertragungs Datentyp an, der zwischen Client und Server übertragen wird.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*repr-Typ* 
</dt> <dd>

Gibt den dargestellten lokalen Typ in der Zielsprache an, die den Client-und Server Anwendungen angezeigt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie **\[ \_ als \]** verwenden, müssen Sie Routinen bereitstellen, die zwischen dem lokalen und dem Übertragungs Typen konvertieren, und den freien Speicherplatz, der zum Speichern der konvertierten Daten verwendet wurde. Das Attribut " **\[ \_ As \]** " weist die stubzeichen an, die vom Benutzer bereitgestellten Konvertierungs Routinen aufzurufen.

Der übertragene Typ mit dem *Namen "-Type* " muss in einen mittleren Basistyp, einen vordefinierten Typ oder einen Typbezeichner aufgelöst werden. Weitere Informationen finden Sie unter [Mittel l-Basis Typen](midl-base-types.md).

Sie müssen die folgenden Routinen angeben:



| Routine Name                   | BESCHREIBUNG                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *benannter \_ Typ * * * \_ from \_ local** | Konvertiert Daten aus dem lokalen Typ in den Netzwerktyp. Die Routine ordnet Arbeitsspeicher für den Netzwerk Datentyp zu, einschließlich des Arbeitsspeichers für alle Daten, auf die von Zeigern im Netzwerk Datentyp verwiesen wird.              |
| *benannter \_ Typ * * * \_ zu \_ lokal**   | Konvertiert Daten aus dem Netzwerktyp in den lokalen Typ. Die Routine ist dafür verantwortlich, Arbeitsspeicher für Daten zuzuweisen, auf die von Zeigern im lokalen Typ verwiesen wird. RPC ordnet Speicher für den lokalen Typ selbst zu. |
| *benannter \_ Typ * * * \_ freie \_ lokale** | Gibt für Daten, auf die von Zeigern im lokalen Typ verwiesen wird, Arbeitsspeicher frei. RPC gibt Arbeitsspeicher für den Typ selbst frei                                                                                             |
| *benannter \_ Typ * * * \_ freie \_ inst**  | Gibt Speicherplatz frei, der für die Daten, auf die von Zeigern im Netzwerktyp verwiesen wird, und für den Netzwerktyp                                                                                            |



 

Der Clientstub Ruft den *benannten Typ * * * \_ aus \_ local** auf, um Speicherplatz für den übertragenen Typ zuzuweisen und die Daten vom lokalen Typ in den Netzwerktyp zu übersetzen. Der Serverstub ordnet Speicherplatz für den ursprünglichen Datentyp zu und ruft den *benannten Typ * * * \_ auf \_ local** auf, um die Daten vom Netzwerktyp in den lokalen Typ zu übersetzen.

Bei Rückgabe aus dem Anwendungscode ruft der Client-und der Server-Stub den *Namen "-Type * * * \_ Free \_ inst**" auf, um die Speicherplatz Zuteilung für den Netzwerktyp freizugeben. Der Clientstub Ruft den *benannten Typ * * * \_ Free \_ local** auf, um die Speicher Belegungs Daten zuzuweisen, die von der Routine zurückgegeben werden.

Die folgenden Typen dürfen kein **\[ \_ als \]** -Attribut darstellen:

-   Konforme, abweichende oder konforme Arrays
-   Strukturen, bei denen der letzte Member ein konformes Array ist (eine konforme Struktur)
-   Zeiger oder Typen, die einen Zeiger enthalten
-   Pipes oder Typen, die Pipes enthalten
-   Typen, die als Basistyp für eine Pipe verwendet werden
-   Vordefinierte Typen [**handle \_ t**](handle-t.md), [**void**](void.md)
-   Typen, die über das [**\[ handle \]**](handle.md) -Attribut verfügen

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

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Handle \_ t**](handle-t.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




