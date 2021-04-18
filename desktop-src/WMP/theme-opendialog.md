---
title: Design. OpenDialog
description: Die OpenDialog-Methode öffnet ein Datei Dialogfeld.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- Design. OpenDialog-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355055"
---
# <a name="themeopendialog"></a><span data-ttu-id="1516b-104">Design. OpenDialog</span><span class="sxs-lookup"><span data-stu-id="1516b-104">THEME.openDialog</span></span>

<span data-ttu-id="1516b-105">Die **OpenDialog** -Methode öffnet ein Datei Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="1516b-105">The **openDialog** method opens a file dialog box.</span></span>

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a><span data-ttu-id="1516b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1516b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1516b-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*DialogType*</span><span class="sxs-lookup"><span data-stu-id="1516b-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span></span>
</dt> <dd>

<span data-ttu-id="1516b-108">Eine **Zeichenfolge** , die den Typ des Dialog Felds angibt.</span><span class="sxs-lookup"><span data-stu-id="1516b-108">A **String** that specifies the type of dialog box.</span></span> <span data-ttu-id="1516b-109">Muss auf "Datei öffnen" festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1516b-109">Must be set to "FILE\_OPEN".</span></span>

</dd> <dt>

<span data-ttu-id="1516b-110"><span id="parameters"></span><span id="PARAMETERS"></span>*Metern*</span><span class="sxs-lookup"><span data-stu-id="1516b-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parameters*</span></span>
</dt> <dd>

<span data-ttu-id="1516b-111">Eine **Zeichenfolge** , die für weitere Informationen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1516b-111">A **String** that can be used for additional information.</span></span> <span data-ttu-id="1516b-112">Muss auf "Files \_ AllMedia" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1516b-112">Must be set to "FILES\_ALLMEDIA".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1516b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1516b-113">Return Value</span></span>

<span data-ttu-id="1516b-114">Diese Methode gibt eine **Zeichenfolge** mit der URL der ausgewählten Datei oder "" (leere Zeichenfolge) zurück, wenn der Benutzer auf Abbrechen klickt.</span><span class="sxs-lookup"><span data-stu-id="1516b-114">This method returns a **String** containing the URL of the selected file or "" (empty string) if the user clicks cancel.</span></span>

## <a name="remarks"></a><span data-ttu-id="1516b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1516b-115">Remarks</span></span>

<span data-ttu-id="1516b-116">Diese Methode kann für Dateien auf den lokalen Festplatten oder auf Netzwerklaufwerken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1516b-116">This method can be used for files on the local hard drives or on network drives.</span></span>

## <a name="examples"></a><span data-ttu-id="1516b-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1516b-117">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="1516b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1516b-118">Requirements</span></span>



| <span data-ttu-id="1516b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1516b-119">Requirement</span></span> | <span data-ttu-id="1516b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1516b-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1516b-121">Version</span><span class="sxs-lookup"><span data-stu-id="1516b-121">Version</span></span><br/> | <span data-ttu-id="1516b-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1516b-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1516b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1516b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1516b-124">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="1516b-124">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





