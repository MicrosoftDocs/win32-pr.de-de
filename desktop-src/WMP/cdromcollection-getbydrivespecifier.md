---
title: Cdromcollection. getbydrivespecifier-Methode
description: Die getbydrivespecifier-Methode ruft das CDROM-Objekt ab, das einem bestimmten Laufwerk Buchstaben zugeordnet ist.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- getbydrivespecifier-Methode, Windows Media Player
- getbydrivespecifier-Methode, Windows Media Player, cdromcollection-Klasse
- Cdromcollection-Klasse, Windows Media Player, getbydrivespecifier-Methode
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370916"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="35c01-106">Cdromcollection. getbydrivespecifier-Methode</span><span class="sxs-lookup"><span data-stu-id="35c01-106">CdromCollection.getByDriveSpecifier method</span></span>

<span data-ttu-id="35c01-107">Die **getbydrivespecifier** -Methode ruft das **CDROM** -Objekt ab, das einem bestimmten Laufwerk Buchstaben zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="35c01-107">The **getByDriveSpecifier** method retrieves the **Cdrom** object associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c01-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="35c01-108">Syntax</span></span>


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a><span data-ttu-id="35c01-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35c01-110">*drivespecifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35c01-110">*driveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35c01-111">**Zeichenfolge** , die den Laufwerk Buchstaben enthält, gefolgt von einem Doppelpunkt (":").</span><span class="sxs-lookup"><span data-stu-id="35c01-111">**String** containing the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35c01-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35c01-112">Return value</span></span>

<span data-ttu-id="35c01-113">Diese Methode gibt ein **CDROM** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="35c01-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="35c01-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35c01-114">Remarks</span></span>

<span data-ttu-id="35c01-115">Laufwerk Buchstaben müssen in der Form *x*: angegeben werden, wobei *x* den Laufwerk Buchstaben darstellt.</span><span class="sxs-lookup"><span data-stu-id="35c01-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="35c01-116">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="35c01-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="35c01-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="35c01-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="35c01-118">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35c01-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="35c01-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35c01-119">Examples</span></span>

<span data-ttu-id="35c01-120">Im folgenden JScript-Beispiel wird *cdromcollection* verwendet. **getbydrivespecifier** zum Abrufen des **CDROM** -Objekts, das einem vom Benutzer bereitgestellten Laufwerk Buchstaben entspricht.</span><span class="sxs-lookup"><span data-stu-id="35c01-120">The following JScript example uses *CdromCollection*.**getByDriveSpecifier** to retrieve the **Cdrom** object that corresponds to a drive letter provided by the user.</span></span> <span data-ttu-id="35c01-121">Für die Benutzereingabe wurde ein HTML-Textelement mit dem Namen "MyText" erstellt.</span><span class="sxs-lookup"><span data-stu-id="35c01-121">An HTML text element was created, with NAME = "MyText", for user input.</span></span> <span data-ttu-id="35c01-122">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="35c01-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a><span data-ttu-id="35c01-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35c01-123">Requirements</span></span>



| <span data-ttu-id="35c01-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35c01-124">Requirement</span></span> | <span data-ttu-id="35c01-125">Wert</span><span class="sxs-lookup"><span data-stu-id="35c01-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35c01-126">Version</span><span class="sxs-lookup"><span data-stu-id="35c01-126">Version</span></span><br/> | <span data-ttu-id="35c01-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="35c01-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="35c01-128">DLL</span><span class="sxs-lookup"><span data-stu-id="35c01-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="35c01-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c01-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35c01-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35c01-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c01-131">**Cdrom-Objekt**</span><span class="sxs-lookup"><span data-stu-id="35c01-131">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="35c01-132">**Cdrom. eject**</span><span class="sxs-lookup"><span data-stu-id="35c01-132">**Cdrom.eject**</span></span>](cdrom-eject.md)
</dt> <dt>

[<span data-ttu-id="35c01-133">**Cdromcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="35c01-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="35c01-134">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="35c01-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="35c01-135">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="35c01-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





