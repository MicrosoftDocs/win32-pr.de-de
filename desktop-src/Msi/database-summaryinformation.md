---
description: Die SummaryInformation-Eigenschaft des Database-Objekts gibt ein SummaryInfo-Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom verwendet werden kann.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Database. SummaryInformation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367183"
---
# <a name="databasesummaryinformation-property"></a><span data-ttu-id="9a8a9-103">Database. SummaryInformation (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9a8a9-103">Database.SummaryInformation property</span></span>

<span data-ttu-id="9a8a9-104">Die **SummaryInformation** -Eigenschaft des [**Database**](database-object.md) -Objekts gibt ein [**SummaryInfo**](summaryinfo-object.md) -Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-104">The **SummaryInformation** property of the [**Database**](database-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the [summary information stream](summary-information-stream.md).</span></span>

<span data-ttu-id="9a8a9-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a8a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a8a9-106">Syntax</span></span>


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="9a8a9-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9a8a9-107">Property value</span></span>

<span data-ttu-id="9a8a9-108">Die maximale Anzahl von Eigenschaften, die hinzugefügt oder geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-108">The maximum number of properties to be added or modified.</span></span> <span data-ttu-id="9a8a9-109">Dieser Parameter ist erforderlich und wird verwendet, um während der Datenstrom Generierung ausreichend Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-109">This parameter is required and used to allocate sufficient working memory during the stream generation.</span></span> <span data-ttu-id="9a8a9-110">Es ist nicht erforderlich, diese Anzahl von Eigenschaften zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-110">It is not required to store this number of properties.</span></span> <span data-ttu-id="9a8a9-111">Wenn die Datenbank schreibgeschützt geöffnet ist, muss der Wert 0 (null) verwendet werden, um zu verhindern, dass der Stream aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-111">A value of zero must be used if the database is opened read-only to prevent the stream from being updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a8a9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a8a9-112">Remarks</span></span>

<span data-ttu-id="9a8a9-113">Wenn ein Wert von *maxproperties* größer als 0 verwendet wird, um einen vorhandenen Zusammenfassungs Informationsdaten Strom zu öffnen, muss die persistente [**Methode vor dem Schließen**](summaryinfo-persist.md) des Objekts aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-113">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="9a8a9-114">Wenn dies nicht der Fall ist, gehen die vorhandenen Datenstrom Informationen verloren.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-114">Failing to do this will lose the existing stream information.</span></span>

<span data-ttu-id="9a8a9-115">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-115">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a8a9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a8a9-116">Requirements</span></span>



| <span data-ttu-id="9a8a9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a8a9-117">Requirement</span></span> | <span data-ttu-id="9a8a9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9a8a9-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8a9-119">Version</span><span class="sxs-lookup"><span data-stu-id="9a8a9-119">Version</span></span><br/> | <span data-ttu-id="9a8a9-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9a8a9-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a8a9-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9a8a9-122">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a8a9-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9a8a9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9a8a9-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a8a9-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a8a9-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9a8a9-125">IID</span><span class="sxs-lookup"><span data-stu-id="9a8a9-125">IID</span></span><br/>     | <span data-ttu-id="9a8a9-126">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9a8a9-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




