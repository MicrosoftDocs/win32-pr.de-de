---
description: 'Flags, die von den Methoden iwiadevmgr:: getimagedlg, IWiaDevMgr2:: getimagedlg, iwiaitem::D evicedlg und IWiaItem2::D evicedlg zum Steuern des Dialogfeld Vorgangs verwendet werden.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: Wiaflag (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348410"
---
# <a name="wiaflag"></a><span data-ttu-id="e40bf-103">Wiaflag</span><span class="sxs-lookup"><span data-stu-id="e40bf-103">WiaFlag</span></span>

<span data-ttu-id="e40bf-104">Flags, die von den Methoden [**iwiadevmgr:: getimagedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: getimagedlg**](-wia-iwiadevmgr2-getimagedlg.md), [**iwiaitem::D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)und [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) zum Steuern des Dialogfeld Vorgangs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e40bf-104">Flags used by the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg), and [**IWiaItem2::DeviceDlg**](-wia-iwiaitem2-devicedlg.md) methods to control the dialog box operation.</span></span>



| <span data-ttu-id="e40bf-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="e40bf-105">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="e40bf-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e40bf-106">Description</span></span>                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <span data-ttu-id="e40bf-107"><dt>**WIA- \_ Geräte \_ Dialogfeld, \_ einzelnes \_ Bild**</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-107"><dt>**WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE**</dt></span></span> </dl>     | <span data-ttu-id="e40bf-108">Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld Geräte Abbild Erfassung.</span><span class="sxs-lookup"><span data-stu-id="e40bf-108">Restrict image selection to a single image in the device image acquisition dialog box.</span></span><br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <span data-ttu-id="e40bf-109"><dt>**Dialog Feld "WIA- \_ Gerät" \_ \_ verwenden \_ allgemeine \_ Benutzeroberfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-109"><dt>**WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI**</dt></span></span> </dl> | <span data-ttu-id="e40bf-110">Verwenden Sie die Benutzeroberfläche des Systems, falls verfügbar, anstelle der vom Hersteller bereitgestellten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="e40bf-110">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="e40bf-111">Wenn die Benutzeroberfläche des Systems nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="e40bf-111">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="e40bf-112">Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="e40bf-112">If neither UI is available, the function returns E\_NOTIMPL.</span></span><br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <span data-ttu-id="e40bf-113"><dt>**WIA \_ Select \_ Device \_ NODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-113"><dt>**WIA\_SELECT\_DEVICE\_NODEFAULT**</dt></span></span> </dl>               | <span data-ttu-id="e40bf-114">Erzwingen Sie die [**iwiadevmgr:: getimagedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) -oder [**IWiaDevMgr2:: getimagedlg**](-wia-iwiadevmgr2-getimagedlg.md) -Methode, um das Dialogfeld **Gerät auswählen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e40bf-114">Force the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) or [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method to display the **Select Device** dialog box.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e40bf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e40bf-115">Requirements</span></span>



| <span data-ttu-id="e40bf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e40bf-116">Requirement</span></span> | <span data-ttu-id="e40bf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e40bf-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e40bf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e40bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e40bf-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e40bf-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e40bf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e40bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e40bf-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e40bf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e40bf-122">Header</span><span class="sxs-lookup"><span data-stu-id="e40bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e40bf-123"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="e40bf-123"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




