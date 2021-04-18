---
description: Gibt den konnenction-Kontext eines mobilen Breitband Geräts an.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: komplexer ContextType-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345709"
---
# <a name="contexttype-complex-type"></a><span data-ttu-id="d5dfc-103">komplexer ContextType-Typ</span><span class="sxs-lookup"><span data-stu-id="d5dfc-103">contextType Complex Type</span></span>

<span data-ttu-id="d5dfc-104">Der komplexe Typ " **ContextType** " gibt den konnenction-Kontext eines mobilen Breitband Geräts an.</span><span class="sxs-lookup"><span data-stu-id="d5dfc-104">The **contextType** complex type specifies the connenction context of a Mobile Broadband device.</span></span>

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d5dfc-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5dfc-105">Child elements</span></span>



| <span data-ttu-id="d5dfc-106">Element</span><span class="sxs-lookup"><span data-stu-id="d5dfc-106">Element</span></span>                                                               | <span data-ttu-id="d5dfc-107">type</span><span class="sxs-lookup"><span data-stu-id="d5dfc-107">Type</span></span>                                           | <span data-ttu-id="d5dfc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5dfc-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5dfc-109">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-109">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)       |                                                | <span data-ttu-id="d5dfc-110">Zum Herstellen einer Datenverbindung zu verwendende APN-oder Wähl Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d5dfc-110">APN or dial string to be used to establish a data connection</span></span><br/>                        |
| [<span data-ttu-id="d5dfc-111">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-111">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)       |                                                | <span data-ttu-id="d5dfc-112">Das Authentifizierungsprotokoll, das zum Aktivieren eines PDP-Kontexts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5dfc-112">Authentication protocol to be used for activating a PDP context.</span></span><br/>                    |
| [<span data-ttu-id="d5dfc-113">**Komprimi**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-113">**Compression**</span></span>](schema-compression-contexttype-element.md)         |                                                | <span data-ttu-id="d5dfc-114">Gibt an, ob die Komprimierung beim Daten Link für Header und Datenübertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5dfc-114">Specifies if compression will be used at the data link for header and data transfer</span></span><br/> |
| [<span data-ttu-id="d5dfc-115">**Ignorepassword**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-115">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="d5dfc-116">boolean</span><span class="sxs-lookup"><span data-stu-id="d5dfc-116">boolean</span></span>                                        | <span data-ttu-id="d5dfc-117">Behandeln von Kenn Wörtern beim Aktualisieren von Profilen</span><span class="sxs-lookup"><span data-stu-id="d5dfc-117">How to handle passwords when upgrading profiles.</span></span><br/>                                    |
| [<span data-ttu-id="d5dfc-118">**Anmelden**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-118">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="d5dfc-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d5dfc-119">string</span></span>                                         | <span data-ttu-id="d5dfc-120">Zum Authentifizieren eines Benutzers verwendetes Kennwort</span><span class="sxs-lookup"><span data-stu-id="d5dfc-120">Password used to authenticate a user</span></span><br/>                                                |
| [<span data-ttu-id="d5dfc-121">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-121">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)     |                                                | <span data-ttu-id="d5dfc-122">Anmelde Informationen für eine Verbindung anmelden.</span><span class="sxs-lookup"><span data-stu-id="d5dfc-122">Log on credentials for a connection.</span></span><br/>                                                |
| [<span data-ttu-id="d5dfc-123">**User**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-123">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="d5dfc-124">**nametype**</span><span class="sxs-lookup"><span data-stu-id="d5dfc-124">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="d5dfc-125">Benutzername für die Anmeldung</span><span class="sxs-lookup"><span data-stu-id="d5dfc-125">User name for logon</span></span><br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="d5dfc-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5dfc-126">Requirements</span></span>



| <span data-ttu-id="d5dfc-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5dfc-127">Requirement</span></span> | <span data-ttu-id="d5dfc-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d5dfc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d5dfc-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5dfc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d5dfc-130">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d5dfc-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d5dfc-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5dfc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d5dfc-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5dfc-132">None supported</span></span><br/>                         |



 

 




