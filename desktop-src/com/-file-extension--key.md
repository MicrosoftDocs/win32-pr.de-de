---
title: file_extension-Taste
description: Ordnet eine Dateinamenerweiterung einer ProgID zu.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856911"
---
# <a name="file_extension-key"></a><span data-ttu-id="13143-103"><Datei \_ Erweiterung> Schlüssel</span><span class="sxs-lookup"><span data-stu-id="13143-103"><file\_extension> Key</span></span>

<span data-ttu-id="13143-104">Ordnet eine Dateinamenerweiterung einer ProgID zu.</span><span class="sxs-lookup"><span data-stu-id="13143-104">Associates a file name extension with a ProgID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="13143-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="13143-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a><span data-ttu-id="13143-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13143-106">Remarks</span></span>

<span data-ttu-id="13143-107">Die im Dateinamen-Erweiterungs Schlüssel enthaltenen Informationen werden sowohl von Windows Explorer als auch von dateimonikern verwendet.</span><span class="sxs-lookup"><span data-stu-id="13143-107">The information contained in the file name extension key is used by both the Windows Explorer and file monikers.</span></span> <span data-ttu-id="13143-108">[**Getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet den Schlüssel für die Dateinamenerweiterung zum Bereitstellen der zugeordneten CLSID.</span><span class="sxs-lookup"><span data-stu-id="13143-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) uses the file name extension key to supply the associated CLSID.</span></span>

<span data-ttu-id="13143-109">Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="13143-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13143-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="13143-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13143-111">**FileType**</span><span class="sxs-lookup"><span data-stu-id="13143-111">**FileType**</span></span>](filetype-key.md)
</dt> <dt>

[<span data-ttu-id="13143-112">**Getclassfile**</span><span class="sxs-lookup"><span data-stu-id="13143-112">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




