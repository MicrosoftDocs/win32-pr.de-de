---
title: Unterstützung für frühe Bindungen
description: Das folgende Codebeispiel zeigt ein Szenario mit einer frühen Bindungs Unterstützung.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, frühe Bindungs Unterstützung
- Binden von AD, frühe Bindungs Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102339"
---
# <a name="early-binding-support"></a>Unterstützung für frühe Bindungen

Das folgende Codebeispiel zeigt ein Szenario mit einer frühen Bindungs Unterstützung.


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



In diesem Codebeispiel erweitern zwei Erweiterungs Komponenten ein **Benutzer** Objekt. Jede Erweiterung veröffentlicht eine eigene Schnittstelle. Jede Erweiterung erkennt die andere Erweiterungsschnittstelle nicht. nur ADSI erkennt, dass beide Erweiterungen vorhanden sind. Jede Erweiterung delegiert Ihr [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) an ADSI. ADSI fungiert als Aggregator für beide Erweiterungen und alle anderen zukünftigen Erweiterungen. Das Abfragen einer Schnittstelle von einer beliebigen Erweiterung oder von ADSI ergibt das gleiche konsistente Ergebnis.

Im folgenden Verfahren wird das Erstellen einer Erweiterung beschrieben.

## <a name="step-1-add-aggregation-to-your-component"></a>Schritt 1: Hinzufügen von Aggregationen zu Ihrer Komponente

Befolgen Sie die com-Spezifikation, um der Komponente Aggregationen hinzuzufügen. Zusammenfassend müssen Sie die *punknown* -Anforderungen Ihrer Komponente während der Erstellung von " **feateinstance**" akzeptieren und den " *punknown* " an den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) des Aggregators delegieren, wenn die Komponente aggregiert wird.

## <a name="step-2-register-your-extension"></a>Schritt 2: Registrieren der Erweiterung

Nun müssen Sie entscheiden, welche Verzeichnis Klasse erweitert werden soll. Sie können nicht die gleichen Schnittstellen verwenden, die Sie für eine ADSI-Schnittstelle verwenden würden, z. b. [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer). Verzeichnisobjekte werden im Verzeichnis gespeichert, während ihre Erweiterung und ADSI auf dem Client Computer ausgeführt werden. Verzeichnis Objekt Beispiele sind " **User**", " **Computer**", " **PrintQueue**", " **serviceConnectionPoint**" und " **ntdsservice**". Sie können in Active Directory eine neue Klasse hinzufügen und eine neue Erweiterung für diese neue Klasse erstellen.

Mithilfe von Registrierungs Schlüsseln ordnen Sie den ADSI-Erweiterungs Komponenten einen Verzeichnis Klassennamen zu. Die folgende Abbildung stellt das vorhandene Registrierungs Layout dar, sowie neue Schlüssel.

-   Ein neuer Schlüssel namens **Erweiterungen** enthält eine Liste von Schlüsseln, von denen jeder eine Klasse im Verzeichnis darstellt. Jede Klasse, z. b. **Benutzer**, **PrintQueue** oder **Computer**, verwaltet eine Liste von unter Schlüsseln.
-   Jeder Unterschlüssel enthält die CLSID der ADSI-Erweiterungs Komponente.
-   Jeder CLSID-Unterschlüssel enthält einen Zeichen folgen Eintrag, der mehrere Werte zulässt. Sie sollten nur die Schnittstellen auflisten, die an der Aggregation beteiligt sind.

> [!Note]  
> Erweiterungs Objekte sind weiterhin erforderlich, um Standard-com-Schlüssel zu registrieren.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a>Beispiel

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

Die Liste der Schnittstellen von Extension1 kann sich von der von Extension2 unterscheiden. Das-Objekt unterstützt die-Schnittstellen des Aggregators (ADSI) und alle Schnittstellen, die vom Extension1 und Extension2 des Aggregats bereitgestellt werden. Auflösung von in Konflikt stehenden Schnittstellen (die gleiche Schnittstelle, die sowohl vom Aggregator als auch von Aggregaten oder mehreren Aggregaten unterstützt wird) wird durch Prioritäten der Erweiterungen bestimmt.

Sie können auch die CLSID-Erweiterung mehreren Objektklassen Namen zuordnen. Beispielsweise kann Ihre Erweiterung sowohl das **Benutzer** -als auch das **Contact** -Objekt erweitern.

> [!Note]  
> Das Erweiterungs Verhalten wird für eine Objektklasse und nicht für eine Objektinstanz hinzugefügt.

 

Als bewährte Vorgehensweise registrieren Sie Ihre Erweiterungen wie alle anderen COM-Komponenten mit einem Aufrufen der **dllregistersvr** -Funktion. Stellen Sie außerdem eine Möglichkeit zum Aufheben der Registrierung ihrer Erweiterung bei der **DllUnregisterServer** -Funktion bereit.

Im folgenden Codebeispiel wird gezeigt, wie eine-Erweiterung registriert wird.


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 