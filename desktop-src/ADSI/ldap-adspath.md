---
title: LDAP-ADsPath
description: Dieses Thema zeigt die Syntax, die Sie für den LDAP-ADsPath verwenden sollten.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- LDAP-ADsPath
- ADsPath, LDAP, Beschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730305"
---
# <a name="ldap-adspath"></a>LDAP-ADsPath

Der ADsPath des Microsoft LDAP-Anbieters erfordert das folgende Format.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> Das linke und das rechte eckige Klammer Zeichen ( \[ \] ) zeigen optionale Parameter an; es handelt sich nicht um einen literalen Teil der Bindungs Zeichenfolge.

 

Bei "Hostname" kann es sich um einen Computernamen, eine IP-Adresse oder einen Domänen Namen handeln. Ein Servername kann auch in der Bindungs Zeichenfolge angegeben werden. Die meisten LDAP-Anbieter folgen einem Modell, für das ein Servername angegeben werden muss.

"PortNumber" gibt den Port an, der für die Verbindung verwendet werden soll. Wenn keine Portnummer angegeben ist, verwendet der LDAP-Anbieter die Standard Portnummer. Die Standard Portnummer ist 389, wenn keine SSL-Verbindung verwendet wird, oder 636 bei Verwendung einer SSL-Verbindung.

"Distinguished shedname" gibt den Distinguished Name eines bestimmten Objekts an. Ein definierter Name für ein bestimmtes Objekt ist garantiert eindeutig.

In der folgenden Tabelle werden Beispiele für das Binden von Zeichen folgen aufgelistet.



| LDAP-ADsPath-Beispiel                                      | BESCHREIBUNG                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| Standardi                                                     | Binden an den Stamm des LDAP-Namespace.                    |
| LDAP://server01                                           | Binden an einen bestimmten Server.                                 |
| LDAP://server01:390                                       | Binden Sie mithilfe der angegebenen Portnummer an einen bestimmten Server. |
| LDAP://CN = Jeff Smith, CN = Users, DC = fabrikam, DC = com          | Binden an ein bestimmtes Objekt.                                 |
| LDAP://Server01/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com | Binden an ein bestimmtes Objekt über einen bestimmten Server.       |



 

Wenn die Kerberos-Authentifizierung erforderlich ist, um eine bestimmte Verzeichnis Anforderung erfolgreich abzuschließen, die Bindungs Zeichenfolge muss entweder einen Server losen ADsPath verwenden, z. b. LDAP://CN = Jeff Smith, CN = Users, DC = fabrikam, DC = com, oder es muss ein ADsPath mit einem voll qualifizierten DNS-Servernamen verwendet werden, z. b. LDAP://Server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com. Die Bindung an den Server mit einem flachen NetBIOS-Namen oder einem kurzen DNS-Namen, z. b. mit dem Namen Server01 anstelle von Server01.fabrikam.com, gewährleistet nicht, dass die Kerberos-Authentifizierung gewährleistet ist.

Weitere Informationen und Beispiele für LDAP-Bindungs Zeichenfolgen sowie eine Beschreibung von Sonderzeichen, die in LDAP-Bindungs Zeichenfolgen verwendet werden können, finden Sie unter LDAP ADsPath.

**Windows 2000 mit SP1 und höher:** Wenn der LDAP-Anbieter eine Bindungs Zeichenfolge mit einem Servernamen enthält, können Sie die Leistung steigern, indem Sie das **ADS- \_ Server \_ Bindungs** Flag mit der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion oder der [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode verwenden. Das **ADS \_ Server \_ Bind** -Flag gibt an, dass ein Servername angegeben wurde, der es ADSI ermöglicht, zusätzlichen, unnötigen Netzwerk Datenverkehr zu vermeiden.

## <a name="ldap-special-characters"></a>LDAP-Sonderzeichen

LDAP verfügt über mehrere Sonderzeichen, die für die Verwendung durch die LDAP-API reserviert sind. Die Liste der Sonderzeichen finden Sie unter [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names). Um eines dieser Zeichen in einem ADsPath zu verwenden, ohne einen Fehler zu erzeugen, muss dem Zeichen ein umgekehrter Schrägstrich () vorangestellt werden \\ . Dies *wird als* Escapezeichen bezeichnet. Wenn z. b. ein Benutzername im Format " <last name> ," angegeben wird <first name> , muss das Komma im Name-Wert mit Escapezeichen versehen werden. Die resultierende Zeichenfolge würde wie folgt aussehen:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



Das Escapezeichen kann auch durch den zweistelligen hexadezimal Zeichencode angegeben werden. Dies wird im folgenden Beispiel gezeigt.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



Nicht druckbare Zeichen, z. b. der Zeilen-und Wagen Rücklauf, müssen mit Escapezeichen versehen und durch ihren zweistelligen hexadezimal Zeichencode angegeben werden. Dies wird im folgenden Beispiel gezeigt.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Weitere Informationen

Weitere Informationen über die von LDAP-kompatiblen Verzeichnisdiensten verwendete Schreibweise von Distinguished Name finden Sie unter [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 