---
title: Zugreifen auf Attribute mit ADSI
description: Die Methoden IADs.Get und IADs.GetEx werden verwendet, um benannte Attributwerte abzurufen.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Attribute, Zugriff mit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e37c63b61986a56e7b22f114b5956d9e047f1ae45b5dc2e653074ea35440f10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024128"
---
# <a name="accessing-attributes-with-adsi"></a>Zugreifen auf Attribute mit ADSI

Die [**Methoden IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) werden verwendet, um benannte Attributwerte abzurufen. Beide Methoden geben einen [**VARIANT-Wert**](/windows/win32/api/oaidl/ns-oaidl-variant) zurück. Diese Methoden sind nur für Verzeichnisse verfügbar, die ein Schema unterstützen. Beim Zugriff auf Objekte in einem Verzeichnis ohne Schema müssen die [**Schnittstellen IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) und [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) verwendet werden, um Attributwerte zu bearbeiten.

Die [**Methoden IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) geben eine VARIANT zurück, die abhängig von der Anzahl der vom Server zurückgegebenen Werte ein [**VARIANT-Array**](/windows/win32/api/oaidl/ns-oaidl-variant) sein kann oder nicht.  Wenn beispielsweise nur ein Wert vom Server zurückgegeben wird, unabhängig davon, ob es sich um ein einzelnes oder ein mehrwertiges Attribut handelt, gibt die Methode eine einzelne **VARIANT-Methode zurück.** Wenn dagegen mehrere Werte zurückgegeben werden, wird ein **VARIANT-Array** zurückgegeben. Wenn ein **VARIANT-Array** zurückgegeben wird, enthält das **vt-Member** der **VARIANT-Struktur** die **Flags VT \_ VARIANT/vbVariant** und **VT \_ ARRAY/vbArray.**

Die [**Methoden IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) können auch über die [**IDispatch-Schnittstelle ein COM-Objekt**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurückgeben. In diesem Fall enthält das **vt-Member** der [**VARIANT-Struktur**](/windows/win32/api/oaidl/ns-oaidl-variant) das **VT \_ DISPATCH/vbObject-Flag.** Um auf das COM-Objekt zu zugreifen, rufen Sie die [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der **IDispatch-Schnittstelle** auf, um die gewünschte Schnittstelle zu erhalten.

Ein weiterer Datentyp, der von den [**Methoden IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) zurückgegeben wird, sind Binärdaten. In diesem Fall werden die Daten als zusammenhängendes Bytearray bereitgestellt, und das **vt-Member** der [**VARIANT-Struktur**](/windows/win32/api/oaidl/ns-oaidl-variant) enthält die **Flags VT \_ UI1/vbByte** und **VT \_ ARRAY/vbArray.**

> [!Note]  
> Microsoft Visual Basic, Scripting Edition unterstützt nur [**VARIANT-**](/windows/win32/api/oaidl/ns-oaidl-variant) und **VARIANT-Arrays.** Aus diesem Grund kann VBScript nicht zum Lesen binärer Eigenschaftswerte verwendet werden.

 

Viele ADSI-Schnittstellen definieren schnittstellenspezifische Eigenschaften. Beispielsweise definiert die [**IADsComputer-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadscomputer) die [**Location-Eigenschaft.**](iadscomputer-property-methods.md) Diese schnittstellendefinierten Eigenschaften können Daten enthalten, die mit einem der benannten Attribute identisch sind, aber die Eigenschaften sind spezifisch für den Objekttyp, auf den die Schnittstelle verweist. In Sprachen, die die Automatisierung unterstützen, kann auf diese schnittstellendefinierten Eigenschaften mithilfe der Punkt notation zugegriffen werden, wie im folgenden Codebeispiel gezeigt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird der Zugriff auf die ADsPath-Eigenschaft auf der IADs-Schnittstelle veranschaulicht.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



In Nichtautomatisierungssprachen müssen die Eigenschaftenzugriffsmethoden für den Zugriff auf die schnittstellendefinierten Eigenschaften verwendet werden. Beispielsweise wird die [**IADsComputer::get \_ Location-Methode**](iadscomputer-property-methods.md) verwendet, um die **IADsComputer.Location-Eigenschaft** abzurufen.

Im folgenden C++-Codebeispiel wird veranschaulicht, wie die Eigenschaftszugriffsmethode in C++ verwendet wird, um den ADsPath eines Benutzers abzurufen.


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



Weitere Informationen zum Zugriff auf Attribute mit ADSI finden Sie unter:

-   [Die Get-Methode](the-get-method.md)
-   [Die GetEx-Methode](the-getex-method.md)
-   [Die GetInfo-Methode](the-getinfo-method.md)
-   [Optimierung mit GetInfoEx](optimization-using-getinfoex.md)
-   [Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Beispielcode zum Lesen von Attributen](example-code-for-reading-attributes.md)

 

 