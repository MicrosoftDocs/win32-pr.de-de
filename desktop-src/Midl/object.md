---
title: Objektattribut
description: Das Attribut \ Object \ Interface identifiziert eine COM-Schnittstelle.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- Objekt Attribut-Mittel l
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb2c21246282646dcf6ae488411316e07ab62b2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726336"
---
# <a name="object-attribute"></a>Objektattribut

Das **\[ Object \]** Interface-Attribut identifiziert eine COM-Schnittstelle. (Eine Schnittstellen Attribut Liste, in der das **\[ Object \]** -Attribut nicht enthalten ist, gibt eine DCE-RPC-Schnittstelle an.)

``` syntax
[ 
    object, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
...    
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeichenfolge-UUID* 
</dt> <dd>

Eine UUID-Zeichenfolge, die vom Hilfsprogramm uuidgen generiert wird. Sie können die UUID-Zeichenfolge in Anführungszeichen einschließen.

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die Schnittstelle als Ganzes angewendet werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Die COM-Schnittstelle, von der diese Schnittstelle abgeleitet ist. Die Basisschnittstelle muss [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)oder eine andere COM-Schnittstelle sein, die entweder direkt oder indirekt von **IUnknown** oder **IDispatch** abgeleitet ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Schnittstellen Attribut Liste für eine COM-Schnittstelle muss das **\[** [**UUID**](uuid.md) - **\]** Attribut enthalten, aber das **\[** [**Versions**](version.md) Attribut kann nicht enthalten sein **\]** .

Standardmäßig generiert das Kompilieren einer COM-Schnittstelle mit dem Mittell-Compiler die Dateien, die zum Erstellen einer Proxy-dll benötigt werden. Diese DLL enthält den Code, der die Verwendung der benutzerdefinierten COM-Schnittstelle sowohl von Client Anwendungen als auch von Objekt Servern unterstützt. Wenn die Schnittstellen Attribut Liste für eine COM-Schnittstelle jedoch das **\[** [**lokale**](local.md) **\]** Attribut angibt, generiert der Mittel l-Compiler nur die Schnittstellen Header Datei.

Der mittlerer l-Compiler generiert automatisch einen Schnittstellen Datentyp für eine COM-Schnittstelle. Als Alternative können Sie [**typedef**](typedef.md) mit dem [**Interface**](interface.md) -Schlüsselwort verwenden, um einen Schnittstellen Datentyp explizit zu definieren. Die Schnittstellen Spezifikation kann dann den Schnittstellen Datentyp in Funktionsparametern und Rückgabe Werten, [**Struktur**](struct.md) -und [**Union**](union.md) -Membern sowie andere Typdeklarationen verwenden. Das folgende Beispiel veranschaulicht die Verwendung eines automatisch generierten [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Datentyps:

``` syntax
[
    object, 
    uuid (ABCDEFOO-1234-1234-5678-ABCDEF123456)
] 
interface IStream : IUnknown
{ 
    typedef IStream * LPSTREAM; 
    // Other interface definition statements.
}
```

In einer COM-Schnittstelle werden alle Schnittstellenmember-Funktionen als virtuelle Funktionen angenommen. Eine virtuelle Funktion weist einen impliziten **this** -Zeiger als ersten Parameter auf. Die virtuelle Funktions Tabelle enthält einen Eintrag für jede Schnittstellenmember-Funktion.

Nicht **\[** [**lokale**](local.md) **\]** objektschnittstellenmember-Funktionen müssen über einen Rückgabewert von HRESULT oder SCODE verfügen. (Beachten Sie, dass in früheren Versionen der in der Mitte zulässigen Member Funktionen " [**void**](void.md)" zurückgegeben wurden. Ab der mittleren Version 3,0 generiert die Rückgabe von **void** jedoch einen Compilerfehler.) Wenn ein Rückgabewert von HRESULT oder SCODE vorhanden ist, wird eine Ausnahme durch die generierten Proxys abgefangen, und der Ausnahme Code wird im Rückgabewert zurückgegeben. Wenn Ihre Anwendung die Fehler ignorieren kann, die während eines Remote Prozedur Aufrufes auftreten, können Sie HRESULT als Rückgabetyp angeben, ohne den Rückgabewert nach dem-Befehl zu überprüfen.

Wenn Sie eine alte Anwendung neu kompilieren, kann das Ändern der Rückgabe Typen zu Problemen mit der Abwärtskompatibilität führen, wenn der Server das neu eingeführte Ergebnis an den Client sendet. Anstatt den Rückgabetyp zu ändern, können Sie die Funktion, die " [**void**](void.md) " zurückgibt, mit dem " **\[** [**\_ Callas**](call-as.md) "- **\]** Attribut bezeichnen und somit zu einer lokalen Funktion führen. Definieren Sie dann eine zugehörige Remote Funktion mit denselben Parametern, aber mit dem Rückgabetyp HRESULT. Die lokale Funktion kann ggf. eine Ausnahme auf Grundlage dieses HRESULT-Werts auslöst.

Das **\[ Object \]** -Attribut ist nicht verfügbar, wenn Sie mit dem/OSF-Schalter des mittleren [](-osf.md) -Compilers kompilieren.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    object
] 
interface IMyInterface : IUnknown
{
    // Interface definition statements.
}

[
    uuid(87654321-1234-1234-1234-123456789ABC), 
    object, 
    local
] 
interface ILocalInterface : ISomeOldCOMInterface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**aufzurufen \_ als**](call-as.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**IID \_ ist**](iid-is.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 