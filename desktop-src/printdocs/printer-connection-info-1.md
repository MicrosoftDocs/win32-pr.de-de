---
description: Stellt Informationen zu einer Verbindung mit einem Drucker dar.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: PRINTER_CONNECTION_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757381"
---
# <a name="printer_connection_info_1-structure"></a><span data-ttu-id="530db-103">Drucker \_ Verbindungs \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="530db-103">PRINTER\_CONNECTION\_INFO\_1 structure</span></span>

<span data-ttu-id="530db-104">Stellt Informationen zu einer Verbindung mit einem Drucker dar.</span><span class="sxs-lookup"><span data-stu-id="530db-104">Represents information about a connection to a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="530db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="530db-105">Syntax</span></span>


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a><span data-ttu-id="530db-106">Member</span><span class="sxs-lookup"><span data-stu-id="530db-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="530db-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="530db-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="530db-108">Die folgenden Werte sind definiert:</span><span class="sxs-lookup"><span data-stu-id="530db-108">The following values are defined:</span></span>



| <span data-ttu-id="530db-109">Wert</span><span class="sxs-lookup"><span data-stu-id="530db-109">Value</span></span>                                      | <span data-ttu-id="530db-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="530db-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="530db-111">Fehler bei der Drucker \_ Verbindung \_ (0x00000020).</span><span class="sxs-lookup"><span data-stu-id="530db-111">PRINTER\_CONNECTION\_MISMATCH (0x00000020)</span></span> | <span data-ttu-id="530db-112">Wenn dieses Bitflag festgelegt ist, stimmt die Druckerverbindung nicht überein.</span><span class="sxs-lookup"><span data-stu-id="530db-112">If this bit-flag is set, the printer connection is mismatched.</span></span> <span data-ttu-id="530db-113">Der Benutzer kann einen lokalen Druckertreiber als *pszdrivername* angeben und ihn verwenden, um das Rendering durchzuführen, anstatt den Treiber zu verwenden, der auf dem Server Drucker installiert ist, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="530db-113">The user can supply a local print driver as *pszDriverName* and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="530db-114">Drucker \_ Verbindung \_ keine \_ Benutzeroberfläche (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="530db-114">PRINTER\_CONNECTION\_NO\_UI (0x00000040)</span></span>   | <span data-ttu-id="530db-115">Wenn dieses Bitflag festgelegt ist, kann dieser Befehl kein Dialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="530db-115">If this bit-flag is set then this call cannot display a dialog box.</span></span> <span data-ttu-id="530db-116">Wenn ein Dialogfeld angezeigt werden muss, um einen Druckertreiber vom Server zu installieren, und dieses Bitflag festgelegt ist, wird der Druckertreiber nicht installiert, die Druckerverbindung wird nicht hinzugefügt, und der-Rückruf schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="530db-116">If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.</span></span><br/> <span data-ttu-id="530db-117">**Windows 7:** Wenn dieses Flag in Windows 7 und höheren Versionen von Windows festgelegt ist und der Benutzer im Modus mit erhöhten Rechten ausgeführt wird, wird das Dialogfeld vertrauenswürdig für **diesen Drucker?** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="530db-117">**Windows 7:** In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the **Do you trust this printer?** dialog will not be shown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="530db-118">**pszdrivername**</span><span class="sxs-lookup"><span data-stu-id="530db-118">**pszDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="530db-119">Ein Zeiger auf den Namen des Treibers.</span><span class="sxs-lookup"><span data-stu-id="530db-119">A pointer to the name of the driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="530db-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="530db-120">Requirements</span></span>



| <span data-ttu-id="530db-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="530db-121">Requirement</span></span> | <span data-ttu-id="530db-122">Wert</span><span class="sxs-lookup"><span data-stu-id="530db-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="530db-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="530db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="530db-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="530db-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="530db-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="530db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="530db-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="530db-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="530db-127">Header</span><span class="sxs-lookup"><span data-stu-id="530db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="530db-128"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="530db-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530db-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="530db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530db-130">Drucken</span><span class="sxs-lookup"><span data-stu-id="530db-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="530db-131">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="530db-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




