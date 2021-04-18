---
description: Die Commit-Methode des Datenbankobjekts schließt die persistente Form der Datenbank ab.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371277"
---
# <a name="databasecommit-method"></a><span data-ttu-id="71857-103">Database. Commit-Methode</span><span class="sxs-lookup"><span data-stu-id="71857-103">Database.Commit method</span></span>

<span data-ttu-id="71857-104">Die **Commit** -Methode des [**Daten Bank**](database-object.md) Objekts schließt die persistente Form der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="71857-104">The **Commit** method of the [**Database**](database-object.md) object finalizes the persistent form of the database.</span></span> <span data-ttu-id="71857-105">Alle persistenten Daten werden in die beschreibbare Datenbank geschrieben, und es werden keine temporären Spalten oder Zeilen geschrieben.</span><span class="sxs-lookup"><span data-stu-id="71857-105">All persistent data is written to the writeable database, and no temporary columns or rows are written.</span></span> <span data-ttu-id="71857-106">Diese Methode hat keine Auswirkungen auf eine Datenbank, die als schreibgeschützt geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="71857-106">This method has no effect on a database opened as read-only.</span></span> <span data-ttu-id="71857-107">Diese Methode kann mehrmals aufgerufen werden, um den aktuellen Status von Tabellen zu speichern, die in den Arbeitsspeicher geladen werden.</span><span class="sxs-lookup"><span data-stu-id="71857-107">This method can be called multiple times to save the current state of tables loaded into memory.</span></span> <span data-ttu-id="71857-108">Wenn die Datenbank schließlich geschlossen wird, wird für alle Änderungen, die nach dem letzten **Commit** vorgenommen werden, ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71857-108">When the database is finally closed, any changes made subsequent to the last **Commit** are rolled back.</span></span> <span data-ttu-id="71857-109">Diese Methode wird normalerweise vor dem Herunterfahren aufgerufen, wenn alle Daten Bank Änderungen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="71857-109">This method is normally called prior to shutdown when all database changes have been finalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="71857-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="71857-110">Syntax</span></span>


```JScript
Database.Commit()
```



## <a name="parameters"></a><span data-ttu-id="71857-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="71857-111">Parameters</span></span>

<span data-ttu-id="71857-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="71857-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71857-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71857-113">Return value</span></span>

<span data-ttu-id="71857-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71857-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71857-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71857-115">Remarks</span></span>

<span data-ttu-id="71857-116">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="71857-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="71857-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71857-117">Requirements</span></span>



| <span data-ttu-id="71857-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71857-118">Requirement</span></span> | <span data-ttu-id="71857-119">Wert</span><span class="sxs-lookup"><span data-stu-id="71857-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71857-120">Version</span><span class="sxs-lookup"><span data-stu-id="71857-120">Version</span></span><br/> | <span data-ttu-id="71857-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71857-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="71857-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71857-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="71857-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="71857-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="71857-124">DLL</span><span class="sxs-lookup"><span data-stu-id="71857-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="71857-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71857-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="71857-126">IID</span><span class="sxs-lookup"><span data-stu-id="71857-126">IID</span></span><br/>     | <span data-ttu-id="71857-127">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="71857-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




