---
title: Objektattribut
description: Das Schnittstellenattribut \object\identifiziert eine COM-Schnittstelle.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- Objektattribut MIDL
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ddf51e020cdcd5d13dde6938a58ea5e51f22d9dd03f8632312b3d6b8453a9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383508"
---
# <a name="object-attribute"></a>Objektattribut

Das **\[ \] Objektschnittstellenattribut** identifiziert eine COM-Schnittstelle. (Eine Schnittstellenattributliste, die das **\[ \] Objektattribut** nicht enthält, gibt eine DCE-RPC-Schnittstelle an.)

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

*string-uuid* 
</dt> <dd>

Eine vom Uuidgen-Hilfsprogramm generierte UUID-Zeichenfolge. Sie können die UUID-Zeichenfolge in Anführungszeichen umschließen.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Andere Attribute, die für die Schnittstelle als Ganzes gelten.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Die COM-Schnittstelle, von der diese Schnittstelle ableitung. Die Basisschnittstelle muss [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)oder eine andere COM-Schnittstelle sein, die entweder direkt oder indirekt von **IUnknown** oder **IDispatch abstammt.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Schnittstellenattributliste für eine COM-Schnittstelle muss das **\[** [**uuid-Attribut**](uuid.md) **\]** enthalten, darf jedoch nicht das **\[** [**Versionsattribut**](version.md) **\]** enthalten.

Standardmäßig werden beim Kompilieren einer COM-Schnittstelle mit dem MIDL-Compiler die Dateien generiert, die zum Erstellen einer Proxy-DLL erforderlich sind. Diese DLL enthält den Code zur Unterstützung der Verwendung der benutzerdefinierten COM-Schnittstelle durch Clientanwendungen und Objektserver. Wenn die Schnittstellenattributliste für eine COM-Schnittstelle jedoch das lokale Attribut angibt, generiert der **\[** [](local.md) **\]** MIDL-Compiler nur die Schnittstellenheaderdatei.

Der MIDL-Compiler generiert automatisch einen Schnittstellendatentyp für eine COM-Schnittstelle. Alternativ können Sie [**typedef**](typedef.md) mit dem Schlüsselwort [**interface**](interface.md) verwenden, um explizit einen Schnittstellendatentyp zu definieren. Die Schnittstellenspezifikation kann dann den Schnittstellendatentyp in Funktionsparametern und [**Rückgabewerten,**](struct.md) Struktur- und [**Union-Membern**](union.md) und anderen Typdeklarationen verwenden. Das folgende Beispiel veranschaulicht die Verwendung [](/windows/desktop/api/objidl/nn-objidl-istream) eines automatisch generierten IStream-Datentyps:

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

In einer COM-Schnittstelle werden alle Schnittstellen-Memberfunktionen als virtuelle Funktionen angenommen. Eine virtuelle Funktion verfügt über einen **impliziten this-Zeiger** als ersten Parameter. Die Virtuelle Funktionstabelle enthält einen Eintrag für jede Schnittstellen-Memberfunktion.

Memberfunktionen **\[** [**der nicht**](local.md) **\]** lokalen Objektschnittstelle müssen über den Rückgabewert HRESULT oder SCODE verfügen. (Beachten Sie, dass frühere Versionen von MIDL memberfunktionen das Zurückgeben von [**void ermöglicht haben.**](void.md) Ab MIDL Version 3.0 generiert die Rückgabe von **void** jedoch einen Compilerfehler.) Der Rückgabewert HRESULT oder SCODE bedeutet, dass die generierten Proxys die Ausnahme abfangen und den Ausnahmecode im Rückgabewert zurückgeben, wenn während eines Remoteaufrufs eine Ausnahme generiert wird. Wenn Ihre Anwendung Fehler ignorieren kann, die während eines Remoteprozeduraufrufs auftreten, können Sie HRESULT als Rückgabetyp angeben, ohne den Rückgabewert nach dem Aufruf zu überprüfen.

Wenn Sie eine alte Anwendung neu kompilieren, kann das Ändern der Rückgabetypen zu Abwärtskompatibilitätsproblemen führen, wenn der Server das neu eingeführte Ergebnis an den Client sendet. Als Alternative zum Ändern des Rückgabetyps können Sie die Funktion, die [**void**](void.md) zurückgibt, mit dem Aufruf als Attribut bezeichnen, wodurch sie zu einer lokalen **\[** [**\_**](call-as.md) **\]** Funktion wird. Definieren Sie dann eine zugehörige Remotefunktion mit den gleichen Parametern, aber mit dem Rückgabetyp HRESULT. Die lokale Funktion kann bei Bedarf eine Ausnahme basierend auf diesem HRESULT-Wert auslösen.

Das **\[ \] Objektattribut** ist nicht verfügbar, wenn Sie mit dem MIDL-Compilerschalter [**/osf kompilieren.**](-osf.md)

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

[**aufrufen \_ als**](call-as.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**iid \_ is**](iid-is.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 