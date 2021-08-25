---
title: IADsClass-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsClass-Schnittstelle erhalten oder legen die folgenden Eigenschaften fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- IADsClass-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8640c6a1d1f12ef959530b72618a503245992fae791dce4e6b9e9aec05bcb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428299"
---
# <a name="iadsclass-property-methods"></a>IADsClass-Eigenschaftenmethoden

Die Eigenschaftenmethoden der [**IADsClass-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsclass) erhalten oder legen die folgenden Eigenschaften fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Zusammenfassung**
</dt> <dd> <dl>

Boolescher Wert, der angibt, ob diese Klasse abstrakt oder nicht abstrakt ist. True **gibt an,** dass diese Klasse eine abstrakte Klasse ist und nicht direkt im Verzeichnisdienst instanziiert werden kann. Abstrakte Klassen können nur als Superklassen verwendet werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BOOLEAN**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**AuxDerivedFrom**
</dt> <dd> <dl>

Array von ADsPath-Zeichenfolgen, die die super Auxiliary-Klassen angeben, von denen diese Klasse ableiten.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Hilfs**
</dt> <dd> <dl>

Boolescher Wert, der angibt, ob diese Klasse "Auxiliary" ist. True **gibt an,** dass diese Klasse eine Auxiliary-Klasse ist und nicht direkt im Verzeichnisdienst instanziiert werden kann. Hilfsklassen können nur als Superklassen anderer Hilfsklassen oder als Quelle zusätzlicher Eigenschaften für strukturelle Klassen verwendet werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BOOLEAN**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**Clsid**
</dt> <dd> <dl>

Optionale anbieterspezifische CLSID, die das COM-Objekt identifiziert, das diese Klasse implementiert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**Container**
</dt> <dd> <dl>

Boolescher Wert, der angibt, ob diese Klasse ein Container anderer Objektklassen sein kann. Wenn dieser Wert **TRUE ist,** können Sie die **get \_ Container-Methode** aufrufen, um ein Array der Objektklassen zu erhalten, die diese Klasse enthalten kann.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BOOLEAN**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**Containment**
</dt> <dd> <dl>

Ein **BSTR-Array,** in dem jedes Element der Name einer Objektklasse ist, die diese Klasse enthalten kann.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**DerivedFrom**
</dt> <dd> <dl>

Array von ADsPath-Zeichenfolgen, die angeben, von welchen Klassen diese Klasse abgeleitet wurde.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**HelpFileContext**
</dt> <dd> <dl>

Kontext-ID in **HelpFileName,** wobei bestimmte Informationen für diese Klasse gefunden werden können.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**HelpFileName**
</dt> <dd> <dl>

Name einer Hilfedatei, die weitere Informationen zu Objekten dieser Klasse enthält.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**MandatoryProperties**
</dt> <dd> <dl>

**SAFEARRAY von** **VARIANT-Objekten,** die die Eigenschaften auflisten, die festgelegt werden müssen, damit diese Klasse in den Speicher geschrieben werden kann. Wenn die Klasse nur eine Eigenschaft enthält, gibt **\_ get MandatoryProperties** einen **BSTR zurück.**

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**NamingProperties**
</dt> <dd> <dl>

**SAFEARRAY von** **BSTR** s, das die Eigenschaften auflistet, die zum Benennen von Attributen dieser Schemaklasse verwendet werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**Oid**
</dt> <dd> <dl>

Anbieterspezifischer Objektbezeichner, der diese Klasse definiert. Dies wird bereitgestellt, um die Schemaerweiterung mithilfe von Active Directory in Verzeichnisdiensten zu ermöglichen, die anbieterspezifische OIDs für Klassen erfordern.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**OptionalProperties**
</dt> <dd> <dl>

**SAFEARRAY von** **VARIANT** s, das die optionalen Eigenschaften für diese Schemaklasse auflistet. Wenn die Klasse nur eine Eigenschaft enthält, gibt **get \_ OptionalProperties** einen **BSTR zurück.**

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**PossibleSuperiors**
</dt> <dd> <dl>

Array von ADsPath-Zeichenfolgen, die die Schemaklassen angeben, die Instanzen dieser Klasse enthalten können.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**PrimaryInterface**
</dt> <dd> <dl>

Optionale anbieterspezifische Bezeichner-GUID, die Objekten dieser Schemaklasse eine Schnittstelle zu ordnet. Beispielsweise wird die Klasse "User", die [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) und **PrimaryInterface** unterstützt, durch **IID \_ IADsUser identifiziert.** Dies muss im standarden Zeichenfolgenformat einer GUID vorliegen, wie von COM definiert. Diese GUID ist der Wert, der in der [**IADs::get \_ GUID-Eigenschaft**](/windows/desktop/api/Iads/nn-iads-iads) in Instanzen dieser Klasse für Anbieter angezeigt wird, die diese Eigenschaft implementieren. Das Identifizieren einer Schemaklasse durch IID der primären Schnittstelle des Klassencodes ermöglicht die Verwendung von **QueryInterface** zur Laufzeit, um zu bestimmen, ob ein Objekt der gewünschten Klasse entspricht.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie die [**IADsClass-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsclass) verwendet wird, um zu bestimmen, ob ein Objekt ein Container sein kann, und listet in diesem Fall die Namen aller enthaltenen Objekte auf.


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



Das folgende Codebeispiel zeigt, wie die [**IADsClass-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsclass) verwendet wird, um zu bestimmen, ob ein Objekt ein Container sein kann, und listet in diesem Fall die Namen aller enthaltenen Objekte auf.


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsClass ist als C8F93DD0-4AE0-11CF-9E73-00AA004A5691 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsClass::Qualifiers**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





