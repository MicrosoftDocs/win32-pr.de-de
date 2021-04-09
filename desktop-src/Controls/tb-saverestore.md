---
title: TB_SAVERESTORE Meldung (kommstrg. h)
description: Senden Sie diese Nachricht, um das Speichern oder Wiederherstellen eines Symbolleisten Zustands zu initiieren.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- Windows-Steuerelemente für TB_SAVERESTORE Meldung
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858637"
---
# <a name="tb_saverestore-message"></a><span data-ttu-id="c974c-104">TB \_ saverestore-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c974c-104">TB\_SAVERESTORE message</span></span>

<span data-ttu-id="c974c-105">Senden Sie diese Nachricht, um das Speichern oder Wiederherstellen eines Symbolleisten Zustands zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="c974c-105">Send this message to initiate saving or restoring a toolbar state.</span></span>

## <a name="parameters"></a><span data-ttu-id="c974c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c974c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c974c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c974c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c974c-108">Flag zum Speichern oder wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="c974c-108">Save or restore flag.</span></span> <span data-ttu-id="c974c-109">Wenn dieser Parameter **true** ist, werden die Informationen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c974c-109">If this parameter is **TRUE**, the information is saved.</span></span> <span data-ttu-id="c974c-110">Wenn der Wert **false** ist, werden die Informationen wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="c974c-110">If it is **FALSE**, the information is restored.</span></span>

</dd> <dt>

<span data-ttu-id="c974c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c974c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c974c-112">Ein Zeiger auf eine [**tbsaveparameams**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) -Struktur, die den Registrierungsschlüssel, den Unterschlüssel und den Wert Namen für die Statusinformationen der Symbolleiste angibt.</span><span class="sxs-lookup"><span data-stu-id="c974c-112">Pointer to a [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) structure that specifies the registry key, subkey, and value name for the toolbar state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c974c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c974c-113">Return value</span></span>

<span data-ttu-id="c974c-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="c974c-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c974c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c974c-115">Remarks</span></span>

<span data-ttu-id="c974c-116">Damit diese Meldung in Version 4,72 und früher zum Speichern oder Wiederherstellen einer Symbolleiste verwendet werden kann, muss das übergeordnete Fenster des Toolbar-Steuer Elements einen Handler für den [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md) -Benachrichtigungs Code implementieren.</span><span class="sxs-lookup"><span data-stu-id="c974c-116">For version 4.72 and earlier, to use this message to save or restore a toolbar, the parent window of the toolbar control must implement a handler for the [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification code.</span></span> <span data-ttu-id="c974c-117">Diese Benachrichtigung wird von der Symbolleiste ausgegeben, um Informationen zu jeder Schaltfläche abzurufen, während Sie wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c974c-117">The toolbar issues this notification to retrieve information about each button as it is restored.</span></span>

<span data-ttu-id="c974c-118">Version 5,80 enthält eine neue Option zum Speichern/Wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="c974c-118">Version 5.80 includes a new save/restore option.</span></span> <span data-ttu-id="c974c-119">Zu Beginn des Vorgangs wird für die Anwendung eine TBN-oder [TBN- \_ Wiederherstellungs](tbn-restore.md) Benachrichtigung angezeigt, sobald die Schaltfläche gespeichert oder wieder hergestellt wird. [ \_ ](tbn-save.md)</span><span class="sxs-lookup"><span data-stu-id="c974c-119">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification.</span></span> <span data-ttu-id="c974c-120">Um diese Option verwenden zu können, müssen Sie Benachrichtigungs Handler implementieren, um der Shell die Bitmap-und Zustandsinformationen zur Verfügung zu stellen, die Sie zum erfolgreichen speichern oder Wiederherstellen des Toolbar-Zustands benötigen.</span><span class="sxs-lookup"><span data-stu-id="c974c-120">To use this option, you must implement notification handlers to provide the Shell with the bitmap and state information it needs to successfully save or restore the toolbar state.</span></span>

## <a name="requirements"></a><span data-ttu-id="c974c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c974c-121">Requirements</span></span>



| <span data-ttu-id="c974c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c974c-122">Requirement</span></span> | <span data-ttu-id="c974c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c974c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c974c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c974c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c974c-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c974c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c974c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c974c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c974c-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c974c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c974c-128">Header</span><span class="sxs-lookup"><span data-stu-id="c974c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c974c-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c974c-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c974c-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c974c-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c974c-131">**TB \_ Saverestorew** (Unicode) und **TB \_ saverestorea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c974c-131">**TB\_SAVERESTOREW** (Unicode) and **TB\_SAVERESTOREA** (ANSI)</span></span><br/>             |



 

 





