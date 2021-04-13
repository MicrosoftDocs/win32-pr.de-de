---
description: Wird mit der Eigenschaften Eigenschaft der UI-Richtlinie der NCrypt verwendet \_ \_ \_ , um Benutzeroberflächen Informationen für einen Schlüssel zu enthalten.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: NCRYPT_UI_POLICY_BLOB Struktur (NCrypt \_ Provider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528727"
---
# <a name="ncrypt_ui_policy_blob-structure"></a><span data-ttu-id="09cd7-103">Ncrypt- \_ UI- \_ Richtlinien- \_ BLOB-Struktur</span><span class="sxs-lookup"><span data-stu-id="09cd7-103">NCRYPT\_UI\_POLICY\_BLOB structure</span></span>

<span data-ttu-id="09cd7-104">Die NCrypt-benutzeroberflächenrichtlinienblob-Struktur wird mit der [**Eigenschaften Eigenschaft NCrypt \_ UI- \_ Richtlinie \_**](key-storage-property-identifiers.md) verwendet, um Benutzeroberflächen Informationen für einen Schlüssel zu enthalten **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="09cd7-104">The **NCRYPT\_UI\_POLICY\_BLOB** structure is used with the [**NCRYPT\_UI\_POLICY\_PROPERTY**](key-storage-property-identifiers.md) property to contain user interface information for a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="09cd7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09cd7-105">Syntax</span></span>


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a><span data-ttu-id="09cd7-106">Member</span><span class="sxs-lookup"><span data-stu-id="09cd7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="09cd7-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="09cd7-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="09cd7-108">Die Versionsnummer der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="09cd7-108">The version number of the structure.</span></span> <span data-ttu-id="09cd7-109">Dieser Member muss 1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="09cd7-109">This member must contain 1.</span></span>

</dd> <dt>

<span data-ttu-id="09cd7-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="09cd7-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="09cd7-111">Ein Satz von Flags, die zusätzliche Informationen oder Anforderungen an die Benutzeroberfläche bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="09cd7-111">A set of flags that provide additional user interface information or requirements.</span></span>



| <span data-ttu-id="09cd7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="09cd7-112">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="09cd7-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="09cd7-113">Meaning</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <span data-ttu-id="09cd7-114"><dt>**NCrypt \_ UI \_ Protect \_ Key- \_ Flag**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="09cd7-114"><dt>**NCRYPT\_UI\_PROTECT\_KEY\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="09cd7-115">Zeigen Sie die Benutzeroberfläche mit starkem Schlüssel nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="09cd7-115">Display the strong key user interface as needed.</span></span><br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <span data-ttu-id="09cd7-116"><dt>**NCrypt \_ \_ \_ \_ \_ Flag**</dt> für die Benutzeroberflächen-Force-Schutz <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="09cd7-116"><dt>**NCRYPT\_UI\_FORCE\_HIGH\_PROTECTION\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="09cd7-117">Erzwingen Sie einen hohen Schutz.</span><span class="sxs-lookup"><span data-stu-id="09cd7-117">Force high protection.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="09cd7-118">**cbkreationtitle**</span><span class="sxs-lookup"><span data-stu-id="09cd7-118">**cbCreationTitle**</span></span>
</dt> <dd>

<span data-ttu-id="09cd7-119">Die Länge (in Byte) des Erstellungs Titels.</span><span class="sxs-lookup"><span data-stu-id="09cd7-119">The length, in bytes, of the creation title.</span></span> <span data-ttu-id="09cd7-120">Der Erstellungs Titel ist eine auf NULL endende Unicode-Zeichenfolge, die den Text angibt, der als Titel des Dialog Felds für den starken Schlüssel verwendet wird, wenn der Schlüssel abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="09cd7-120">The creation title is a null-terminated Unicode string that specifies the text that is used as the title of the strong key dialog box when the key is completed.</span></span> <span data-ttu-id="09cd7-121">Der Erstellungs Titel muss direkt nach der **blobstruktur der NCrypt- \_ UI- \_ Richtlinie \_** platziert werden.</span><span class="sxs-lookup"><span data-stu-id="09cd7-121">The creation title must be placed immediately following the **NCRYPT\_UI\_POLICY\_BLOB** structure.</span></span> <span data-ttu-id="09cd7-122">Wenn der Wert des **cbkreationtitle** -Members auf 0 festgelegt ist, wird ein standardmäßiger Erstellungs Titel für den Titel des Dialog Felds für den starken Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="09cd7-122">If the value of the **cbCreationTitle** member is set to 0, a default creation title is used for the title of the strong key dialog box.</span></span> <span data-ttu-id="09cd7-123">Dieser Member wird nur bei der Schlüssel Finalisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="09cd7-123">This member is only used on key finalization.</span></span>

</dd> <dt>

<span data-ttu-id="09cd7-124">**cbfriendlyname**</span><span class="sxs-lookup"><span data-stu-id="09cd7-124">**cbFriendlyName**</span></span>
</dt> <dd>

<span data-ttu-id="09cd7-125">Die Länge (in Byte) des anzeigen Amens des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="09cd7-125">The length, in bytes, of the friendly name of the key.</span></span> <span data-ttu-id="09cd7-126">Der Anzeige Name ist eine NULL-terminierte Unicode-Zeichenfolge, die den Text enthält, der im Dialogfeld für den starken Schlüssel als Name des Schlüssels angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="09cd7-126">The friendly name is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the name of the key.</span></span> <span data-ttu-id="09cd7-127">Der Anzeige Name muss direkt nach dem Erstellungs Titel in diesem BLOB platziert werden.</span><span class="sxs-lookup"><span data-stu-id="09cd7-127">The friendly name must be placed immediately following the creation title in this BLOB.</span></span> <span data-ttu-id="09cd7-128">Wenn der Wert des Members **cbfriendlyname** auf 0 festgelegt ist, wird im Dialogfeld für den starken Schlüssel ein Standardname verwendet.</span><span class="sxs-lookup"><span data-stu-id="09cd7-128">If the value of the **cbFriendlyName** member is set to 0, a default name is used in the strong key dialog box.</span></span> <span data-ttu-id="09cd7-129">Dieser Member wird sowohl verwendet, wenn der Schlüssel abgeschlossen ist, als auch, wenn der Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09cd7-129">This member is used both when the key is completed and when the key is used.</span></span>

</dd> <dt>

<span data-ttu-id="09cd7-130">**cbdescription**</span><span class="sxs-lookup"><span data-stu-id="09cd7-130">**cbDescription**</span></span>
</dt> <dd>

<span data-ttu-id="09cd7-131">Die Länge (in Byte) der Schlüssel Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="09cd7-131">The length, in bytes, of the key description.</span></span> <span data-ttu-id="09cd7-132">Die Schlüssel Beschreibung ist eine mit NULL endenden Unicode-Zeichenfolge, die den Text enthält, der im Dialogfeld für den starken Schlüssel als die Beschreibung des Schlüssels angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="09cd7-132">The key description is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the description of the key.</span></span> <span data-ttu-id="09cd7-133">Der Beschreibungs Wert muss direkt nach dem anzeigen Amen in diesem BLOB eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="09cd7-133">The description value must be placed immediately following the friendly name in this BLOB.</span></span> <span data-ttu-id="09cd7-134">Wenn der Wert des **cbdescription** -Members auf 0 festgelegt ist, wird im Dialogfeld für den starken Schlüssel eine Standardbeschreibung verwendet.</span><span class="sxs-lookup"><span data-stu-id="09cd7-134">If the value of the **cbDescription** member is set to 0, a default description is used in the strong key dialog box.</span></span> <span data-ttu-id="09cd7-135">Dieser Member wird sowohl verwendet, wenn der Schlüssel abgeschlossen ist, als auch, wenn der Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09cd7-135">This member is used both when the key is completed and when the key is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09cd7-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09cd7-136">Remarks</span></span>

<span data-ttu-id="09cd7-137">Diese Struktur ist im NCrypt \_ Provider. h-Header enthalten.</span><span class="sxs-lookup"><span data-stu-id="09cd7-137">This structure is included in the Ncrypt\_provider.h header.</span></span> <span data-ttu-id="09cd7-138">Um die Struktur zu verwenden, müssen Sie das [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) von Microsoft Connect herunterladen.</span><span class="sxs-lookup"><span data-stu-id="09cd7-138">To use the structure, you must download the [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) from Microsoft Connect.</span></span>

## <a name="requirements"></a><span data-ttu-id="09cd7-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09cd7-139">Requirements</span></span>



| <span data-ttu-id="09cd7-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09cd7-140">Requirement</span></span> | <span data-ttu-id="09cd7-141">Wert</span><span class="sxs-lookup"><span data-stu-id="09cd7-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="09cd7-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09cd7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="09cd7-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09cd7-143">Windows Vista \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="09cd7-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09cd7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="09cd7-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09cd7-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="09cd7-146">Header</span><span class="sxs-lookup"><span data-stu-id="09cd7-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="09cd7-147"><dt>Ncrypt- \_ Anbieter. h</dt></span><span class="sxs-lookup"><span data-stu-id="09cd7-147"><dt>Ncrypt\_provider.h</dt></span></span> </dl> |



 

