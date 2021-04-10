---
title: Dialog Feld Funktionen
description: .
ms.assetid: 7ea6445a-1772-4986-b4b7-27512afa680d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 789e450e0a6e42157f0036f5d1e805856fcc8b95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039577"
---
# <a name="dialog-box-functions"></a><span data-ttu-id="97e39-103">Dialog Feld Funktionen</span><span class="sxs-lookup"><span data-stu-id="97e39-103">Dialog Box Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="97e39-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="97e39-104">In this section</span></span>

-   [<span data-ttu-id="97e39-105">**"Kreatedialog"**</span><span class="sxs-lookup"><span data-stu-id="97e39-105">**CreateDialog**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialoga)
-   [<span data-ttu-id="97e39-106">**"Kreatedialogindirect"**</span><span class="sxs-lookup"><span data-stu-id="97e39-106">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="97e39-107">**"Kreatedialogindirectparam"**</span><span class="sxs-lookup"><span data-stu-id="97e39-107">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="97e39-108">**"Kreatedialogparam"**</span><span class="sxs-lookup"><span data-stu-id="97e39-108">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
-   [<span data-ttu-id="97e39-109">**Defdlgproc**</span><span class="sxs-lookup"><span data-stu-id="97e39-109">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
-   [<span data-ttu-id="97e39-110">**Dialogbox**</span><span class="sxs-lookup"><span data-stu-id="97e39-110">**DialogBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxa)
-   [<span data-ttu-id="97e39-111">**Dialogboxindirekte**</span><span class="sxs-lookup"><span data-stu-id="97e39-111">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="97e39-112">**Dialogboxderedereparam**</span><span class="sxs-lookup"><span data-stu-id="97e39-112">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
-   [<span data-ttu-id="97e39-113">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="97e39-113">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
-   [<span data-ttu-id="97e39-114">*DialogProc*</span><span class="sxs-lookup"><span data-stu-id="97e39-114">*DialogProc*</span></span>](/windows/win32/api/winuser/nc-winuser-dlgproc)
-   [<span data-ttu-id="97e39-115">**EndDialog**</span><span class="sxs-lookup"><span data-stu-id="97e39-115">**EndDialog**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enddialog)
-   [<span data-ttu-id="97e39-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="97e39-116">**GetDialogBaseUnits**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits)
-   [<span data-ttu-id="97e39-117">**Getdlgctrlid**</span><span class="sxs-lookup"><span data-stu-id="97e39-117">**GetDlgCtrlID**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid)
-   [<span data-ttu-id="97e39-118">**GetDlgItem**</span><span class="sxs-lookup"><span data-stu-id="97e39-118">**GetDlgItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitem)
-   [<span data-ttu-id="97e39-119">**Getdlgitemint**</span><span class="sxs-lookup"><span data-stu-id="97e39-119">**GetDlgItemInt**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint)
-   [<span data-ttu-id="97e39-120">**Getdlgitemtext**</span><span class="sxs-lookup"><span data-stu-id="97e39-120">**GetDlgItemText**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta)
-   [<span data-ttu-id="97e39-121">**Getnextdlggroupitem**</span><span class="sxs-lookup"><span data-stu-id="97e39-121">**GetNextDlgGroupItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem)
-   [<span data-ttu-id="97e39-122">**Getnextdlgtabitem**</span><span class="sxs-lookup"><span data-stu-id="97e39-122">**GetNextDlgTabItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem)
-   [<span data-ttu-id="97e39-123">**IsDialogMessage**</span><span class="sxs-lookup"><span data-stu-id="97e39-123">**IsDialogMessage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea)
-   [<span data-ttu-id="97e39-124">**Mapdialogrect**</span><span class="sxs-lookup"><span data-stu-id="97e39-124">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
-   [<span data-ttu-id="97e39-125">**MessageBox**</span><span class="sxs-lookup"><span data-stu-id="97e39-125">**MessageBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messagebox)
-   [<span data-ttu-id="97e39-126">**Messageboxex**</span><span class="sxs-lookup"><span data-stu-id="97e39-126">**MessageBoxEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)
-   [<span data-ttu-id="97e39-127">**Messageboxindirekte**</span><span class="sxs-lookup"><span data-stu-id="97e39-127">**MessageBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messageboxindirecta)
-   [<span data-ttu-id="97e39-128">**SendDlgItemMess age**</span><span class="sxs-lookup"><span data-stu-id="97e39-128">**SendDlgItemMessage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea)
-   [<span data-ttu-id="97e39-129">**Setdlgitemint**</span><span class="sxs-lookup"><span data-stu-id="97e39-129">**SetDlgItemInt**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint)
-   [<span data-ttu-id="97e39-130">**SetDlgItemText**</span><span class="sxs-lookup"><span data-stu-id="97e39-130">**SetDlgItemText**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta)

 

 