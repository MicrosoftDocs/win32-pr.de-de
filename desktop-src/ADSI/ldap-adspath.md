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
# <a name="ldap-adspath"></a><span data-ttu-id="cc627-105">LDAP-ADsPath</span><span class="sxs-lookup"><span data-stu-id="cc627-105">LDAP ADsPath</span></span>

<span data-ttu-id="cc627-106">Der ADsPath des Microsoft LDAP-Anbieters erfordert das folgende Format.</span><span class="sxs-lookup"><span data-stu-id="cc627-106">The Microsoft LDAP provider ADsPath requires the following format.</span></span>


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> <span data-ttu-id="cc627-107">Das linke und das rechte eckige Klammer Zeichen ( \[ \] ) zeigen optionale Parameter an; es handelt sich nicht um einen literalen Teil der Bindungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc627-107">The left and right bracket characters (\[ \]) indicate optional parameters; it is not a literal part of the binding string.</span></span>

 

<span data-ttu-id="cc627-108">Bei "Hostname" kann es sich um einen Computernamen, eine IP-Adresse oder einen Domänen Namen handeln.</span><span class="sxs-lookup"><span data-stu-id="cc627-108">The "HostName" can be a computer name, an IP address, or a domain name.</span></span> <span data-ttu-id="cc627-109">Ein Servername kann auch in der Bindungs Zeichenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc627-109">A server name can also be specified in the binding string.</span></span> <span data-ttu-id="cc627-110">Die meisten LDAP-Anbieter folgen einem Modell, für das ein Servername angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="cc627-110">Most LDAP providers follow a model that requires a server name to be specified.</span></span>

<span data-ttu-id="cc627-111">"PortNumber" gibt den Port an, der für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc627-111">The "PortNumber" specifies the port to be used for the connection.</span></span> <span data-ttu-id="cc627-112">Wenn keine Portnummer angegeben ist, verwendet der LDAP-Anbieter die Standard Portnummer.</span><span class="sxs-lookup"><span data-stu-id="cc627-112">If no port number is specified, the LDAP provider uses the default port number.</span></span> <span data-ttu-id="cc627-113">Die Standard Portnummer ist 389, wenn keine SSL-Verbindung verwendet wird, oder 636 bei Verwendung einer SSL-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cc627-113">The default port number is 389 if not using an SSL connection or 636 if using an SSL connection.</span></span>

<span data-ttu-id="cc627-114">"Distinguished shedname" gibt den Distinguished Name eines bestimmten Objekts an.</span><span class="sxs-lookup"><span data-stu-id="cc627-114">The "DistinguishedName" specifies the distinguished name of a specific object.</span></span> <span data-ttu-id="cc627-115">Ein definierter Name für ein bestimmtes Objekt ist garantiert eindeutig.</span><span class="sxs-lookup"><span data-stu-id="cc627-115">A distinguished name for a given object is guaranteed to be unique.</span></span>

<span data-ttu-id="cc627-116">In der folgenden Tabelle werden Beispiele für das Binden von Zeichen folgen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cc627-116">The following table lists examples of binding strings.</span></span>



| <span data-ttu-id="cc627-117">LDAP-ADsPath-Beispiel</span><span class="sxs-lookup"><span data-stu-id="cc627-117">LDAP ADsPath example</span></span>                                      | <span data-ttu-id="cc627-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc627-118">Description</span></span>                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cc627-119">Standardi</span><span class="sxs-lookup"><span data-stu-id="cc627-119">LDAP:</span></span>                                                     | <span data-ttu-id="cc627-120">Binden an den Stamm des LDAP-Namespace.</span><span class="sxs-lookup"><span data-stu-id="cc627-120">Bind to the root of the LDAP namespace.</span></span>                    |
| <span data-ttu-id="cc627-121">LDAP://server01</span><span class="sxs-lookup"><span data-stu-id="cc627-121">LDAP://server01</span></span>                                           | <span data-ttu-id="cc627-122">Binden an einen bestimmten Server.</span><span class="sxs-lookup"><span data-stu-id="cc627-122">Bind to a specific server.</span></span>                                 |
| <span data-ttu-id="cc627-123">LDAP://server01:390</span><span class="sxs-lookup"><span data-stu-id="cc627-123">LDAP://server01:390</span></span>                                       | <span data-ttu-id="cc627-124">Binden Sie mithilfe der angegebenen Portnummer an einen bestimmten Server.</span><span class="sxs-lookup"><span data-stu-id="cc627-124">Bind to a specific server using the specified port number.</span></span> |
| <span data-ttu-id="cc627-125">LDAP://CN = Jeff Smith, CN = Users, DC = fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="cc627-125">LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span>          | <span data-ttu-id="cc627-126">Binden an ein bestimmtes Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc627-126">Bind to a specific object.</span></span>                                 |
| <span data-ttu-id="cc627-127">LDAP://Server01/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="cc627-127">LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span> | <span data-ttu-id="cc627-128">Binden an ein bestimmtes Objekt über einen bestimmten Server.</span><span class="sxs-lookup"><span data-stu-id="cc627-128">Bind to a specific object through a specific server.</span></span>       |



 

<span data-ttu-id="cc627-129">Wenn die Kerberos-Authentifizierung erforderlich ist, um eine bestimmte Verzeichnis Anforderung erfolgreich abzuschließen, die Bindungs Zeichenfolge muss entweder einen Server losen ADsPath verwenden, z. b. LDAP://CN = Jeff Smith, CN = Users, DC = fabrikam, DC = com, oder es muss ein ADsPath mit einem voll qualifizierten DNS-Servernamen verwendet werden, z. b. LDAP://Server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="cc627-129">If Kerberos authentication is required for the successful completion of a specific directory request, the binding string must use either a serverless ADsPath, such as LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, or it must use an ADsPath with a fully qualified DNS server name, such as LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com.</span></span> <span data-ttu-id="cc627-130">Die Bindung an den Server mit einem flachen NetBIOS-Namen oder einem kurzen DNS-Namen, z. b. mit dem Namen Server01 anstelle von Server01.fabrikam.com, gewährleistet nicht, dass die Kerberos-Authentifizierung gewährleistet ist.</span><span class="sxs-lookup"><span data-stu-id="cc627-130">Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the name server01 instead of server01.fabrikam.com, is not guaranteed to yield Kerberos authentication.</span></span>

<span data-ttu-id="cc627-131">Weitere Informationen und Beispiele für LDAP-Bindungs Zeichenfolgen sowie eine Beschreibung von Sonderzeichen, die in LDAP-Bindungs Zeichenfolgen verwendet werden können, finden Sie unter LDAP ADsPath.</span><span class="sxs-lookup"><span data-stu-id="cc627-131">For more information and examples of LDAP binding strings, as well as a description of special characters that can be used in LDAP binding strings, see LDAP ADsPath.</span></span>

<span data-ttu-id="cc627-132">**Windows 2000 mit SP1 und höher:** Wenn der LDAP-Anbieter eine Bindungs Zeichenfolge mit einem Servernamen enthält, können Sie die Leistung steigern, indem Sie das **ADS- \_ Server \_ Bindungs** Flag mit der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion oder der [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc627-132">**Windows 2000 with SP1 and later:** With the LDAP provider, if a binding string includes a server name, you can increase performance by using the **ADS\_SERVER\_BIND** flag with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="cc627-133">Das **ADS \_ Server \_ Bind** -Flag gibt an, dass ein Servername angegeben wurde, der es ADSI ermöglicht, zusätzlichen, unnötigen Netzwerk Datenverkehr zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cc627-133">The **ADS\_SERVER\_BIND** flag indicates that a server name was specified, which enables ADSI to avoid additional, unnecessary network traffic.</span></span>

## <a name="ldap-special-characters"></a><span data-ttu-id="cc627-134">LDAP-Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="cc627-134">LDAP Special Characters</span></span>

<span data-ttu-id="cc627-135">LDAP verfügt über mehrere Sonderzeichen, die für die Verwendung durch die LDAP-API reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="cc627-135">LDAP has several special characters which are reserved for use by the LDAP API.</span></span> <span data-ttu-id="cc627-136">Die Liste der Sonderzeichen finden Sie unter [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="cc627-136">The list of special characters can be found in [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span> <span data-ttu-id="cc627-137">Um eines dieser Zeichen in einem ADsPath zu verwenden, ohne einen Fehler zu erzeugen, muss dem Zeichen ein umgekehrter Schrägstrich () vorangestellt werden \\ .</span><span class="sxs-lookup"><span data-stu-id="cc627-137">To use one of these characters in an ADsPath without generating an error, the character must be preceded by a backslash (\\) character.</span></span> <span data-ttu-id="cc627-138">Dies *wird als* Escapezeichen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cc627-138">This is known as *escaping* the character.</span></span> <span data-ttu-id="cc627-139">Wenn z. b. ein Benutzername im Format " <last name> ," angegeben wird <first name> , muss das Komma im Name-Wert mit Escapezeichen versehen werden.</span><span class="sxs-lookup"><span data-stu-id="cc627-139">For example, if a user name is given in the form of "<last name>,<first name>", the comma in the name value must be escaped.</span></span> <span data-ttu-id="cc627-140">Die resultierende Zeichenfolge würde wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="cc627-140">The resulting string would look like this:</span></span>


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="cc627-141">Das Escapezeichen kann auch durch den zweistelligen hexadezimal Zeichencode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc627-141">The escaped character can also be specified by its two digit hexadecimal character code.</span></span> <span data-ttu-id="cc627-142">Dies wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc627-142">This is shown in the following example.</span></span>


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="cc627-143">Nicht druckbare Zeichen, z. b. der Zeilen-und Wagen Rücklauf, müssen mit Escapezeichen versehen und durch ihren zweistelligen hexadezimal Zeichencode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc627-143">Non-printable characters, such as the line feed and carriage return, must be escaped and specified by their two digit hexadecimal character code.</span></span> <span data-ttu-id="cc627-144">Dies wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc627-144">This is shown in the following example.</span></span>


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a><span data-ttu-id="cc627-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc627-145">For More Information</span></span>

<span data-ttu-id="cc627-146">Weitere Informationen über die von LDAP-kompatiblen Verzeichnisdiensten verwendete Schreibweise von Distinguished Name finden Sie unter [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .</span><span class="sxs-lookup"><span data-stu-id="cc627-146">For more information about the distinguished name notation used by LDAP-compliant directory services, see [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt).</span></span>

 

 