---
description: Die OpenLog-Methode des Merge-Objekts öffnet eine Protokolldatei, die Status-und Fehlermeldungen empfängt. Wenn die Protokolldatei bereits vorhanden ist, fügt das Installationsprogramm neue Nachrichten an. Wenn die Protokolldatei nicht vorhanden ist, erstellt das Installationsprogramm eine Protokolldatei.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Merge. OpenLog-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370873"
---
# <a name="mergeopenlog-method"></a><span data-ttu-id="c79e1-105">Merge. OpenLog-Methode</span><span class="sxs-lookup"><span data-stu-id="c79e1-105">Merge.OpenLog method</span></span>

<span data-ttu-id="c79e1-106">Die **OpenLog** -Methode des [**Merge**](merge-object.md) -Objekts öffnet eine Protokolldatei, die Status-und Fehlermeldungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c79e1-106">The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages.</span></span> <span data-ttu-id="c79e1-107">Wenn die Protokolldatei bereits vorhanden ist, fügt das Installationsprogramm neue Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="c79e1-107">If the log file already exists, the installer appends new messages.</span></span> <span data-ttu-id="c79e1-108">Wenn die Protokolldatei nicht vorhanden ist, erstellt das Installationsprogramm eine Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="c79e1-108">If the log file does not exist, the installer creates a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79e1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c79e1-109">Syntax</span></span>


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a><span data-ttu-id="c79e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c79e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79e1-111">*Filename*</span><span class="sxs-lookup"><span data-stu-id="c79e1-111">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="c79e1-112">Voll qualifizierter Dateiname, der auf eine Datei verweist, die geöffnet oder erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c79e1-112">Fully qualified file name pointing to a file to open or create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c79e1-113">Return value</span></span>

<span data-ttu-id="c79e1-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c79e1-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79e1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c79e1-115">Remarks</span></span>

<span data-ttu-id="c79e1-116">Clients können Ihre eigenen Nachrichten über die [**Log**](merge-log.md) -Methode an diese Protokolldatei senden.</span><span class="sxs-lookup"><span data-stu-id="c79e1-116">Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.</span></span>

### <a name="c"></a><span data-ttu-id="c79e1-117">C++</span><span class="sxs-lookup"><span data-stu-id="c79e1-117">C++</span></span>

<span data-ttu-id="c79e1-118">Siehe [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c79e1-118">See [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c79e1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c79e1-119">Requirements</span></span>



| <span data-ttu-id="c79e1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c79e1-120">Requirement</span></span> | <span data-ttu-id="c79e1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c79e1-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c79e1-122">Version</span><span class="sxs-lookup"><span data-stu-id="c79e1-122">Version</span></span><br/> | <span data-ttu-id="c79e1-123">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c79e1-123">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c79e1-124">Header</span><span class="sxs-lookup"><span data-stu-id="c79e1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c79e1-125"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79e1-125"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c79e1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c79e1-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c79e1-127"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c79e1-127"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
