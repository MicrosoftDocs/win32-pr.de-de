---
title: Bindungs Zeichenfolge
description: Aufgrund der Anzahl von Objekten, auf die von einem Verzeichnisdienst aus zugegriffen werden kann, können Namenskollisionen auftreten.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Bindungs Zeichenfolge ADSI
- ADsPath ADSI, Beschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949106"
---
# <a name="binding-string"></a>Bindungs Zeichenfolge

Aufgrund der Anzahl von Objekten, auf die von einem Verzeichnisdienst aus zugegriffen werden kann, können Namenskollisionen auftreten. Die Bindungs Zeichenfolge, die im Allgemeinen als ADsPath bezeichnet wird, ermöglicht es Ihnen, ein bestimmtes Objekt anzugeben, ohne einen namens Konflikt zu verursachen. Dies kann für einen einzelnen Verzeichnis Dienstanbieter oder für mehrere Verzeichnis Dienstanbieter angewendet werden.

Ein ADsPath ist eine Zeichenfolge, die ein ADSI-Objekt in einem Verzeichnisdienst eindeutig identifiziert. Da ADSI-Objekte innerhalb des Kontexts des Namespace des zugrunde liegenden Verzeichnis Dienstanbieters vorhanden sind, ist ein Teil der Syntax eines ADsPath-namens Anbieter spezifisch.

In der folgenden Tabelle sind die standardmäßig bereitgestellten ADSI-Anbieter aufgelistet.



| Anbieter         | Beschreibung                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WinNT<br/> | Wird zur Kommunikation mit Windows-Domänen Controllern verwendet. Weitere Informationen zu WinNT ADsPath finden Sie unter [Winnt ADsPath](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Wird für die Kommunikation mit LDAP-Servern verwendet, z. b. Active Directory. Weitere Informationen zum LDAP-ADsPath finden Sie unter [LDAP ADsPath](ldap-adspath.md).<br/>  |
| Teams<br/>   | Stellt eine [**iadsnamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) -Implementierung bereit, die zum Auflisten aller auf dem Client installierten ADSI-Anbieter verwendet werden kann.<br/> |



 

Verwenden Sie diese Anbieter Namen, um auf den Standard Namespace des Anbieters zuzugreifen. Wenn Sie z. b. eine Bindung an LDAP herstellen, bindet ADSI an einen Container, der das derzeit angemeldete Domänen Objekt enthält. Wenn Sie eine Bindung an WinNT herstellen, bindet ADSI eine Bindung an einen Container mit Objekten, die mit allen Domänen im Netzwerk korrelieren.

Die ursprünglichen Elemente der ADsPath-Zeichenfolge sind der Programm Bezeichner (ProgID) des ADSI-Anbieters, gefolgt von "://", gefolgt von der Syntax, die vom Anbieter Namespace vorgegeben wird. Die ProgID-Zeichenfolge kann je nach Anbieter die Groß-/Kleinschreibung beachten. Die ProgID-Zeichen folgen für die oben aufgeführten Anbieter unterliegen der Groß-/Kleinschreibung.

Die Pfad Zeichenfolge kann je nach Anbieter die Groß-/Kleinschreibung beachten. Die Pfad Zeichenfolgen für die oben aufgeführten Anbieter unterliegen nicht der Groß-/Kleinschreibung.

Im folgenden finden Sie Beispiele für adspaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Wenn Sie alle auf dem Computer installierten Anbieter suchen möchten, binden Sie ihn an den ADS-Anbieter, wie im folgenden Codebeispiel gezeigt.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Mithilfe des LDAP-Anbieters können Sie den ADsPath entweder in einem DN-Formular (X. 500 Distinguished Name) angeben, beginnend mit dem CN-Tag, oder Sie können die hierarchische Umkehrung angeben, beginnend mit dem O-Tag. Das Formular, das Sie in der anfänglichen ADsPath-Anwendung verwenden, bestimmt die Reihenfolge der Tags.

In der folgenden Tabelle werden ADsPath-Sonderzeichen aufgelistet.



| Name                      | Zeichen           | BESCHREIBUNG                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Doppeltes Anführungszeichen<br/>   | "<br/>        | Wird verwendet, um einen Teil des ADsPath anzugeben, der möglicherweise ein Sonderzeichen enthält, sodass die Zeichenfolge buchstäblich interpretiert wird. Beispiel: "CN = Name/prefix".<br/>                                     |
| Umgekehrter Schrägstrich<br/>      | \\<br/>       | Wird für Sonderzeichen verwendet, um anzugeben, dass Sie als Literale verwendet werden sollen. Weitere Informationen und eine Liste von Sonderzeichen finden Sie unter [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).<br/> |
| ßen<br/>          | /<br/>        | Komponenten Trennzeichen.<br/>                                                                                                                                                                       |
| Geschweifte Klammern<br/> | <><br/> | Begrenzen Sie einen ADsPath innerhalb einer anderen Benennungs Konvention.<br/>                                                                                                                                       |



 

Wenn Sie einen ADsPath in einer Such Spezifikation oder als Teil einer URL begrenzen möchten, verwenden Sie die linke und die Rechte Spitze Klammer (< >). Beispiel: " &lt; Winnt://mydomain/Useraccount &gt; ".

Einige ADSI-Anbieter haben aufgrund von Namespace Anforderungen möglicherweise Syntax Einschränkungen hinzugefügt.

## <a name="active-directory-binding-options"></a>Bindungs Optionen Active Directory

Active Directory bietet die Möglichkeit, an ein Objekt zu binden, indem es verschiedene andere Typen von Bindungs Zeichenfolgen verwendet, z. b. eine com-Globally Unique Identifier (GUID) oder eine Sicherheits-ID (SID). Weitere Informationen finden Sie unter [binden an Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).

 

