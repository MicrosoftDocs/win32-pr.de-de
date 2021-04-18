---
title: UI_ALL_COMMANDS (uiribbon. h)
description: Gibt eine Konstante an, die die Auflistung der Befehle identifiziert, die in der Markup Ressourcen Datei deklariert sind.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340782"
---
# <a name="ui_all_commands"></a><span data-ttu-id="91cb7-103">UI \_ All- \_ Befehle</span><span class="sxs-lookup"><span data-stu-id="91cb7-103">UI\_ALL\_COMMANDS</span></span>

<span data-ttu-id="91cb7-104">Gibt eine Konstante an, die die Auflistung der Befehle identifiziert, die in der Markup Ressourcen Datei deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="91cb7-104">Specifies a constant that identifies the collection of Commands declared in the Markup resource file.</span></span>

## <a name="remarks"></a><span data-ttu-id="91cb7-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91cb7-105">Remarks</span></span>

<span data-ttu-id="91cb7-106">**Benutzeroberfläche \_ Alle \_ Befehle** sind nützlich, wenn es erforderlich ist, auf ähnliche Eigenschaften über alle Befehle zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="91cb7-106">**UI\_ALL\_COMMANDS** is useful when it is necessary to access similar properties across all Commands.</span></span> <span data-ttu-id="91cb7-107">Beispielsweise können **UI \_ All- \_ Befehle** an [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) übergeben werden, um alle Menü Band Befehle für ungültig zu erklären und zu aktualisieren, indem die Host Anwendung nach neuen Eigenschafts Werten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="91cb7-107">For example, **UI\_ALL\_COMMANDS** can be passed to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) to invalidate and refresh all Ribbon Commands by querying the host application for new property values.</span></span>

## <a name="requirements"></a><span data-ttu-id="91cb7-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91cb7-108">Requirements</span></span>



| <span data-ttu-id="91cb7-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91cb7-109">Requirement</span></span> | <span data-ttu-id="91cb7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="91cb7-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91cb7-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91cb7-111">Minimum supported client</span></span><br/> | <span data-ttu-id="91cb7-112">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91cb7-112">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="91cb7-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91cb7-113">Minimum supported server</span></span><br/> | <span data-ttu-id="91cb7-114">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91cb7-114">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="91cb7-115">Header</span><span class="sxs-lookup"><span data-stu-id="91cb7-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="91cb7-116"><dt>Uiribbon. h</dt></span><span class="sxs-lookup"><span data-stu-id="91cb7-116"><dt>Uiribbon.h</dt></span></span> </dl>                                             |
| <span data-ttu-id="91cb7-117">IDL</span><span class="sxs-lookup"><span data-stu-id="91cb7-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91cb7-118"><dt>Uiribbon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91cb7-118"><dt>Uiribbon.idl</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="91cb7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91cb7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91cb7-120">Konstanten und Enumerationen</span><span class="sxs-lookup"><span data-stu-id="91cb7-120">Constants and Enumerations</span></span>](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

