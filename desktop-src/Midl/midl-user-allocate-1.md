---
title: midl_user_allocate-Attribut
description: Die Funktion "Mittelwert \_ Benutzer \_ zuweisen" ist eine Funktion, die Client-und Server Anwendungen bereitstellen, um Speicher zuzuweisen.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate Attribut-Mittel l
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315062"
---
# <a name="midl_user_allocate-attribute"></a>Attribut "Mittel l- \_ Benutzer \_ zuweisen"

Die Funktion " **Mittelwert \_ Benutzer \_ zuweisen** " ist eine Funktion, die Client-und Server Anwendungen bereitstellen, um Speicher zuzuweisen.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*cbytes* 
</dt> <dd>

Gibt die Anzahl der zuzuordnenden Bytes an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sowohl Client Anwendungen als auch Server Anwendungen müssen die Funktion " **mittlere \_ \_ Benutzer** Zuordnungen" implementieren, es sei denn, Sie kompilieren ihn im OSF-Kompatibilitätsmodus ([**/OSF**](-osf.md)). Anwendungen und generierte stubzeichen wenden beim Umgang mit Objekten, auf die von Zeigern verwiesen wird, eine **mittlere \_ Benutzer \_ Zuteilung** an

-   Die Serveranwendung sollte bei der Erstellung eines neuen Knotens für die Application-Klasse den Befehl " **Mittel l- \_ Benutzer \_ zuweisen** " anrufen.
-   Der Serverstub Ruft beim Marshalling von referenzierten Daten in den Adressraum des Servers die Benutzer Zuordnungen für **mittellose \_ Benutzer \_** auf.
-   Der Clientstub Ruft bei der Aufhebung des Marshalling von Daten von dem Server, auf den von einem [**out**](out-idl.md) -Zeiger verwiesen wird, die Benutzer Zuordnungen für **mittlere \_ Benutzer \_** auf Beachten Sie, dass **\[** [](in.md) **\]** der Client-Stub bei in-, **\[ \] out**-und **\[** [**Unique**](unique.md) **\]** -Zeigern nur dann die **\_ Benutzer \_** Zuordnungen aufruft, wenn der **\[ eindeutige \]** Zeiger Wert bei Eingabe **null** war und während des Aufrufs zu einem Wert ungleich **null** wechselt. Wenn der **\[ eindeutige \]** Zeiger bei Eingabe ungleich **null** war, schreibt der Clientstub die zugeordneten Daten in den vorhandenen Arbeitsspeicher.

Wenn die Zuordnungen von **\_ Benutzer \_** Zuordnungen keinen Arbeitsspeicher zuordnen können, muss ein **null** -Zeiger zurückgegeben werden.

Es wird empfohlen, dass die Benutzer Zuordnungen in der Mitte einen Zeiger zurückgeben, der auf 8 Bytes ausgerichtet ist. **\_ \_**

## <a name="examples"></a>Beispiele


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**mittlerer l- \_ Benutzer \_ kostenlos**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 