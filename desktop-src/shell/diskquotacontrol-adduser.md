---
description: Weist einem neuen Benutzer ein nicht standardmäßiges Datenträger Kontingent zu.
title: Diskquotacontrol. AddUser-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525337"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="4c7f5-103">Diskquotacontrol. AddUser-Methode</span><span class="sxs-lookup"><span data-stu-id="4c7f5-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="4c7f5-104">Weist einem neuen Benutzer ein nicht standardmäßiges Datenträger Kontingent zu.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c7f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c7f5-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="4c7f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c7f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c7f5-107">*slogonname*</span><span class="sxs-lookup"><span data-stu-id="4c7f5-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7f5-108">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="4c7f5-108">Type: **CHAR**</span></span>

<span data-ttu-id="4c7f5-109">Ein Zeichen folgen Wert, der den Anmelde Namen des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="4c7f5-110">Verwenden Sie die [**usernameresolution**](diskquotacontrol-usernameresolution.md) -Eigenschaft, um anzugeben, wie der Name aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c7f5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c7f5-111">Return value</span></span>

<span data-ttu-id="4c7f5-112">Type: **Object**</span><span class="sxs-lookup"><span data-stu-id="4c7f5-112">Type: **Object**</span></span>

<span data-ttu-id="4c7f5-113">Gibt einen Objekt Ausdruck zurück, der das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers ergibt.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7f5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c7f5-114">Remarks</span></span>

<span data-ttu-id="4c7f5-115">Das NTFS-Dateisystem erstellt automatisch einen Benutzer Kontingent Eintrag, wenn ein Benutzer zum ersten Mal auf das Volume schreibt.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="4c7f5-116">Einträge, die auf diese Weise erstellt werden, werden die Standardwerte für Warnungs Schwellenwert und feste Kontingent Grenze für das Volume zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="4c7f5-117">Mit dieser Methode können Sie einen Benutzer Kontingent Eintrag erstellen, bevor ein Benutzerinformationen in das Volume schreibt.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="4c7f5-118">Er gibt ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt zurück, das verwendet werden kann, um einen Warnungs Schwellenwert oder einen Kontingent Grenzwert zuzuweisen, der sich von den Standardeinstellungen für das Volume unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="4c7f5-119">Wenn der Benutzer bereits vorhanden ist, wird kein neuer Eintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="4c7f5-120">Die-Methode gibt das [**didiskquotauser**](didiskquotauser-object.md) -Objekt zurück, das dem vorhandenen Eintrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4c7f5-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7f5-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4c7f5-121">Requirements</span></span>



| <span data-ttu-id="4c7f5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c7f5-122">Requirement</span></span> | <span data-ttu-id="4c7f5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4c7f5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7f5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c7f5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7f5-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c7f5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c7f5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c7f5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7f5-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c7f5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4c7f5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4c7f5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c7f5-129"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4c7f5-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c7f5-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4c7f5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7f5-131">**Defaultquotalimit**</span><span class="sxs-lookup"><span data-stu-id="4c7f5-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="4c7f5-132">**Defaultquotathreshold**</span><span class="sxs-lookup"><span data-stu-id="4c7f5-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="4c7f5-133">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4c7f5-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




