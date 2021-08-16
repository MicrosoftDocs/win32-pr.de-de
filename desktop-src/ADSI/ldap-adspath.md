---
title: LDAP-ADsPath
description: In diesem Thema wird die Syntax gezeigt, die Sie für LDAP-ADsPath verwenden sollten.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- LDAP-ADsPath
- ADsPath, LDAP, Beschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1850c30ff8a5a086fbd697080ac32b5e55549496739d9388a6d5e7ab251403d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839470"
---
# <a name="ldap-adspath"></a>LDAP-ADsPath

Der Microsoft LDAP-Anbieter ADsPath erfordert das folgende Format.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> Die linken und rechten eckigen Zeichen \[ \] () geben optionale Parameter an. Es handelt sich nicht um einen Literalteil der Bindungszeichenfolge.

 

"HostName" kann ein Computername, eine IP-Adresse oder ein Domänenname sein. Ein Servername kann auch in der Bindungszeichenfolge angegeben werden. Die meisten LDAP-Anbieter folgen einem Modell, für das ein Servername angegeben werden muss.

"PortNumber" gibt den Port an, der für die Verbindung verwendet werden soll. Wenn keine Portnummer angegeben wird, verwendet der LDAP-Anbieter die Standardportnummer. Die Standardportnummer ist 389, wenn keine SSL-Verbindung verwendet wird, oder 636, wenn eine SSL-Verbindung verwendet wird.

"DistinguishedName" gibt den Distinguished Name eines bestimmten Objekts an. Ein Distinguished Name für ein bestimmtes Objekt ist garantiert eindeutig.

In der folgenden Tabelle sind Beispiele für Bindungszeichenfolgen aufgeführt.



| LDAP-ADsPath-Beispiel                                      | Beschreibung                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| Ldap:                                                     | Binden Sie an den Stamm des LDAP-Namespace.                    |
| LDAP://server01                                           | Binden an einen bestimmten Server.                                 |
| LDAP://server01:390                                       | Binden Sie mithilfe der angegebenen Portnummer an einen bestimmten Server. |
| LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com          | Binden an ein bestimmtes Objekt.                                 |
| LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com | Binden an ein bestimmtes Objekt über einen bestimmten Server.       |



 

Wenn die Kerberos-Authentifizierung für den erfolgreichen Abschluss einer bestimmten Verzeichnisanforderung erforderlich ist, muss die Bindungszeichenfolge entweder einen serverlosen ADsPath verwenden, z. B. LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, oder sie muss einen ADsPath mit einem vollqualifizierten DNS-Servernamen verwenden, z. B. LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com. Die Bindung an den Server mit einem flachen NETBIOS-Namen oder einem kurzen DNS-Namen, z. B. mit dem Namen server01 anstelle von server01.fabrikam.com, ist nicht garantiert, dass die Kerberos-Authentifizierung erfolgt.

Weitere Informationen und Beispiele für LDAP-Bindungszeichenfolgen sowie eine Beschreibung von Sonderzeichen, die in LDAP-Bindungszeichenfolgen verwendet werden können, finden Sie unter LDAP-ADsPath.

**Windows 2000 mit SP1 und höher:** Wenn eine Bindungszeichenfolge mit dem LDAP-Anbieter einen Servernamen enthält, können Sie die Leistung mithilfe des **ADS \_ SERVER \_ BIND-Flags** mit der [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder der [**IADsOpenDSObject::OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) steigern. Das **ADS \_ SERVER \_ BIND-Flag** gibt an, dass ein Servername angegeben wurde, wodurch ADSI zusätzlichen, unnötigen Netzwerkdatenverkehr vermeiden kann.

## <a name="ldap-special-characters"></a>LDAP-Sonderzeichen

LDAP verfügt über mehrere Sonderzeichen, die für die Verwendung durch die LDAP-API reserviert sind. Die Liste der Sonderzeichen finden Sie unter [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names). Um eines dieser Zeichen in einem ADsPath zu verwenden, ohne einen Fehler zu generieren, muss dem Zeichen ein umgekehrter Schrägstrich () vorangestellt \\ werden. Dies wird *alsCaping* des Zeichens bezeichnet. Wenn beispielsweise ein Benutzername in der Form " , " angegeben <last name> <first name> wird, muss das Komma im Namenswert mit Escapeinformationen versehen werden. Die resultierende Zeichenfolge würde wie folgt aussehen:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



Das Escapezeichen kann auch durch den hexadezimalen Zeichencode mit zwei Ziffern angegeben werden. Dies wird im folgenden Beispiel gezeigt.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



Nicht druckbare Zeichen, z. B. Zeilenvorschub und Wagenrücklauf, müssen mit Escapezeichen und durch ihren zweistelligen Hexadezimalzeichencode angegeben werden. Dies wird im folgenden Beispiel gezeigt.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Weitere Informationen

Weitere Informationen zur Distinguished Name-Notation, die von LDAP-kompatiblen Verzeichnisdiensten verwendet wird, finden Sie unter [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 