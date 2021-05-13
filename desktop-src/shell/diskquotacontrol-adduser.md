---
description: Weist einem neuen Benutzer ein nicht standardmäßiges Datenträgerkontingent zu.
title: DiskQuotaControl.AddUser-Methode
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
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841531"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="da8f6-103">DiskQuotaControl.AddUser-Methode</span><span class="sxs-lookup"><span data-stu-id="da8f6-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="da8f6-104">Weist einem neuen Benutzer ein nicht standardmäßiges Datenträgerkontingent zu.</span><span class="sxs-lookup"><span data-stu-id="da8f6-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="da8f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da8f6-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="da8f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da8f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da8f6-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="da8f6-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="da8f6-108">Typ: **CHAR**</span><span class="sxs-lookup"><span data-stu-id="da8f6-108">Type: **CHAR**</span></span>

<span data-ttu-id="da8f6-109">Ein Zeichenfolgenwert, der den Anmeldenamen des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="da8f6-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="da8f6-110">Verwenden Sie die [**UserNameResolution-Eigenschaft,**](diskquotacontrol-usernameresolution.md) um anzugeben, wie der Name aufgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="da8f6-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da8f6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da8f6-111">Return value</span></span>

<span data-ttu-id="da8f6-112">Typ: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="da8f6-112">Type: **Object**</span></span>

<span data-ttu-id="da8f6-113">Gibt einen Objektausdruck zurück, der das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) des Benutzers ergibt.</span><span class="sxs-lookup"><span data-stu-id="da8f6-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="da8f6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da8f6-114">Remarks</span></span>

<span data-ttu-id="da8f6-115">Das NTFS-Dateisystem erstellt automatisch einen Benutzerkontingenteintrag, wenn ein Benutzer zum ersten Mal auf das Volume schreibt.</span><span class="sxs-lookup"><span data-stu-id="da8f6-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="da8f6-116">Einträgen, die auf diese Weise erstellt werden, werden der Standardmäßige Warnungsschwellenwert und die Festgelegten Kontingentgrenzwerte für das Volume zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="da8f6-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="da8f6-117">Mit dieser Methode können Sie einen Benutzerkontingenteintrag erstellen, bevor ein Benutzer Informationen auf das Volume schreibt.</span><span class="sxs-lookup"><span data-stu-id="da8f6-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="da8f6-118">Es wird ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurückgegeben, mit dem ein Warnungsschwellenwert oder ein Kontingentgrenzwert zugewiesen werden kann, der sich von den Standardeinstellungen für das Volume unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="da8f6-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="da8f6-119">Wenn der Benutzer bereits vorhanden ist, wird kein neuer Eintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="da8f6-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="da8f6-120">Die -Methode gibt das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) zurück, das dem vorhandenen Eintrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="da8f6-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="da8f6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da8f6-121">Requirements</span></span>



| <span data-ttu-id="da8f6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da8f6-122">Requirement</span></span> | <span data-ttu-id="da8f6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="da8f6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da8f6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da8f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="da8f6-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da8f6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da8f6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da8f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="da8f6-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da8f6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="da8f6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="da8f6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da8f6-129"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="da8f6-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8f6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da8f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8f6-131">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="da8f6-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="da8f6-132">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="da8f6-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="da8f6-133">**DiskQuotaControl-Objekt**</span><span class="sxs-lookup"><span data-stu-id="da8f6-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




