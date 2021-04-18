---
description: Wird zum Konfigurieren von CAPICOM-Komponenten verwendet.
title: Einstellungs Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372149"
---
# <a name="settings-object-cryptography"></a><span data-ttu-id="7a356-103">Einstellungs Objekt (Kryptografie)</span><span class="sxs-lookup"><span data-stu-id="7a356-103">Settings object (Cryptography)</span></span>

<span data-ttu-id="7a356-104">\[Das **Einstellungs** Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="7a356-104">\[The **Settings** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="7a356-105">Das **Einstellungs** Objekt wird verwendet, um CAPICOM-Komponenten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7a356-105">The **Settings** object is used to configure CAPICOM components.</span></span>

## <a name="members"></a><span data-ttu-id="7a356-106">Member</span><span class="sxs-lookup"><span data-stu-id="7a356-106">Members</span></span>

<span data-ttu-id="7a356-107">Das **Einstellungs** Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7a356-107">The **Settings** object has these types of members:</span></span>

-   [<span data-ttu-id="7a356-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a356-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a356-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a356-109">Properties</span></span>

<span data-ttu-id="7a356-110">Das **Einstellungs** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a356-110">The **Settings** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7a356-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7a356-111">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7a356-112">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="7a356-112">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7a356-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a356-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="7a356-114"><a href="settings-activedirectorysearchlocation.md"><strong>Activedirectoriysearchlocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a356-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a356-115">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a356-115">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a356-116">Legt den Active Directory Suchspeicherort fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="7a356-116">Sets or retrieves the Active Directory search location.</span></span> <span data-ttu-id="7a356-117">Der ursprüngliche Speicherort ist standardmäßig nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="7a356-117">The initial location is unspecified by default.</span></span> <span data-ttu-id="7a356-118">Wenn der Speicherort nicht angegeben ist, wird der globale Katalog durchsucht, und die Standard Domäne wird durchsucht.</span><span class="sxs-lookup"><span data-stu-id="7a356-118">When the location is unspecified, the global catalog is searched, then the default domain is searched.</span></span> <span data-ttu-id="7a356-119">Die Suche bestimmt, ob das Attribut des Benutzer Zertifikats an diesem Speicherort veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="7a356-119">The search determines whether the user certificate attribute is published at that location.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="7a356-120"><a href="settings-enablepromptforcertificateui.md"><strong>Enablepromptforcertifiereui</strong></a></span><span class="sxs-lookup"><span data-stu-id="7a356-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a356-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a356-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="7a356-122">Legt einen booleschen Wert fest, der angibt, ob Benutzeroberflächen Aufforderungen für die Identität eines Signatur Gebers oder Absenders verwendet werden können, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="7a356-122">Sets or retrieves a Boolean value that indicates whether user interface prompts for a signer or sender's identity can be used.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7a356-123">Wenn Sie diese Eigenschaft festlegen, werden Warnungen nicht deaktiviert, die generiert werden, bevor die Verwendung von privaten Schlüsseln aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7a356-123">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7a356-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a356-124">Remarks</span></span>

<span data-ttu-id="7a356-125">Das **Einstellungs** Objekt kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="7a356-125">The **Settings** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="7a356-126">Die ProgID für das **Einstellungs** Objekt ist "CAPICOM". Einstellungen. 1.</span><span class="sxs-lookup"><span data-stu-id="7a356-126">The ProgID for the **Settings** object is CAPICOM.Settings.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a356-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a356-127">Requirements</span></span>



| <span data-ttu-id="7a356-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a356-128">Requirement</span></span> | <span data-ttu-id="7a356-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7a356-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a356-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7a356-130">Redistributable</span></span><br/> | <span data-ttu-id="7a356-131">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a356-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7a356-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7a356-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="7a356-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a356-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a356-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a356-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a356-135">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="7a356-135">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 




