---
title: Bindungszeichenfolge
description: Aufgrund der Anzahl von Objekten, auf die über einen Verzeichnisdienst zugegriffen werden kann, können Namenskonflikte auftreten.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Bindungszeichenfolge ADSI
- ADsPath ADSI , Beschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8e1bc59011c1279b340348572fa0681a0d301319f75603b73714df4c9cb96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023688"
---
# <a name="binding-string"></a>Bindungszeichenfolge

Aufgrund der Anzahl von Objekten, auf die über einen Verzeichnisdienst zugegriffen werden kann, können Namenskonflikte auftreten. Mit der Bindungszeichenfolge, die häufig als ADsPath bezeichnet wird, können Sie ein bestimmtes Objekt angeben, ohne einen Namenskonflikt zu verursachen. Dies kann für einen einzelnen Verzeichnisdienstanbieter oder für mehrere Verzeichnisdienstanbieter angewendet werden.

Ein ADsPath ist eine Zeichenfolge, die ein ADSI-Objekt in einem Verzeichnisdienst eindeutig identifiziert. Da ADSI-Objekte im Kontext des Namespace des zugrunde liegenden Verzeichnisdiensts vorhanden sind, ist ein Teil der Syntax eines ADsPath-Namens anbieterspezifisch.

In der folgenden Tabelle sind die standardmäßig bereitgestellten ADSI-Anbieter aufgeführt.



| Anbieter         | Beschreibung                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Winnt<br/> | Wird für die Kommunikation mit Windows Domänencontrollern verwendet. Weitere Informationen zu WinNT ADsPath finden Sie unter [WinNT ADsPath](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Wird für die Kommunikation mit LDAP-Servern wie Active Directory verwendet. Weitere Informationen zum LDAP-ADsPath finden Sie unter [LDAP ADsPath](ldap-adspath.md).<br/>  |
| Anzeigen<br/>   | Stellt eine [**IADsNamespaces-Implementierung**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) zur Enumerierung aller auf dem Client installierten ADSI-Anbieter zur Anwendung.<br/> |



 

Verwenden Sie diese Anbieternamen, um auf den Standardnamespace des Anbieters zuzugreifen. Wenn Sie beispielsweise eine Bindung an LDAP herstellen, wird ADSI an einen Container gebunden, der das derzeit angemeldete Domänenobjekt enthält. Wenn Sie eine Bindung an WinNT vornehmen, wird ADSI an einen Container gebunden, der Objekte enthält, die mit allen Domänen im Netzwerk korrelieren.

Die anfänglichen Elemente der ADsPath-Zeichenfolge sind der programmgesteuerte Bezeichner (progID) des ADSI-Anbieters, gefolgt von "://", gefolgt von der vom Anbieternamespace diktierten Syntax. Bei der ProgID-Zeichenfolge wird je nach Anbieter möglicherweise die Kleinschreibung beachtet oder nicht. Bei den progID-Zeichenfolgen für die oben aufgeführten Anbieter wird die Kleinschreibung beachtet.

Bei der Pfadzeichenfolge wird je nach Anbieter möglicherweise die Kleinschreibung beachtet oder nicht. Bei den Pfadzeichenfolgen für die oben aufgeführten Anbieter wird die Kleinschreibung nicht beachtet.

Im Folgenden finden Sie Beispiele für ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Um alle auf Ihrem Computer installierten Anbieter zu finden, binden Sie an den ADs-Anbieter, wie im folgenden Codebeispiel gezeigt.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Mit dem LDAP-Anbieter können Sie den ADsPath entweder in einem DN-Format (X.500 Distinguished Name) angeben, beginnend mit dem CN-Tag, oder Sie können dessen hierarchische Umkehrung angeben, beginnend mit dem O-Tag. Das Formular, das Sie im anfänglichen ADsPath verwenden, bestimmt die Reihenfolge der Tags.

In der folgenden Tabelle sind die ADsPath-Sonderzeichen aufgeführt.



| Name                      | Zeichen           | BESCHREIBUNG                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Doppeltes Anführungszeichen<br/>   | "<br/>        | Wird zum Anführungszeichen eines beliebigen Teils des ADsPath verwendet, der ein Sonderzeichen enthalten kann, sodass die Zeichenfolge wörtlich interpretiert wird. Beispiel: "CN=Name/Präfix".<br/>                                     |
| Umgekehrter Schrägstrich<br/>      | \\<br/>       | Wird verwendet, um Sonderzeichen vorangehende Zeichen zu geben, die als Literale verwendet werden sollen. Weitere Informationen und eine Liste mit Sonderzeichen finden Sie unter [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).<br/> |
| Schrägstrich<br/>          | /<br/>        | Komponententrennzeichen.<br/>                                                                                                                                                                       |
| Geschweifte Klammern<br/> | <><br/> | Begrenzen Sie einen ADsPath innerhalb einer anderen Benennungskonvention.<br/>                                                                                                                                       |



 

Um einen ADsPath in einer Suchspezifikation oder als Teil einer URL zu begrenzen, verwenden Sie die linke und rechte eckige Klammer (< >). Beispiel: " &lt; WinNT://MyDomain/UserAccount &gt; ".

Einige ADSI-Anbieter haben aufgrund von Namespaceanforderungen möglicherweise Syntaxeinschränkungen hinzugefügt.

## <a name="active-directory-binding-options"></a>Active Directory-Bindungsoptionen

Active Directory bietet die Möglichkeit, eine Bindung an ein Objekt mithilfe mehrerer anderer Arten von Bindungszeichenfolgen zu erstellen, z. B. mithilfe einer COM-GUID (Globally Unique Identifier) oder einer Sicherheits-ID (SID). Weitere Informationen finden Sie unter [Binden an Active Directory.](/windows/desktop/AD/binding-to-active-directory-domain-services)

 

