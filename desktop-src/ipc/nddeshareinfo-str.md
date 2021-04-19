---
description: Enthält DDE-Freigabe Attribute, die vom NetDDE-Freigabe Datenbank-Manager (DSDM) verwaltet werden.
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Ndbeshareingefo-Struktur (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364197"
---
# <a name="nddeshareinfo-structure"></a><span data-ttu-id="86665-103">Ndbeshareingefo-Struktur</span><span class="sxs-lookup"><span data-stu-id="86665-103">NDDESHAREINFO structure</span></span>

<span data-ttu-id="86665-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86665-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="86665-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="86665-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="86665-106">Enthält DDE-Freigabe Attribute, die vom NetDDE-Freigabe Datenbank-Manager (DSDM) verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="86665-106">Contains DDE share attributes maintained by the NetDDE Share Database Manager (DSDM).</span></span> <span data-ttu-id="86665-107">Die Sicherheits Beschreibung, die den einzelnen DDE-Freigaben zugeordnet ist, wird nicht über diese Struktur, sondern über bestimmte Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="86665-107">The security descriptor associated with each DDE share is not passed through this structure but is accessed through specific functions.</span></span> <span data-ttu-id="86665-108">Die NetDDE-DSDM-API akzeptiert diese Struktur für Set-Funktionen. für Get-Funktionen gibt die DSDM die Struktur, die in den angegebenen Puffer gepackt ist, zusammen mit den Daten zurück, auf die von den Membern **lpszsharename**, **lpszapptopiclist** und **lpszitemlist** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="86665-108">The NetDDE DSDM API accepts this structure for set functions; for get functions, the DSDM returns the structure packed into the supplied buffer along with the data referenced by the members **lpszShareName**, **lpszAppTopicList**, and **lpszItemList**.</span></span>

## <a name="syntax"></a><span data-ttu-id="86665-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="86665-109">Syntax</span></span>


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a><span data-ttu-id="86665-110">Member</span><span class="sxs-lookup"><span data-stu-id="86665-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="86665-111">**lrevision**</span><span class="sxs-lookup"><span data-stu-id="86665-111">**lRevision**</span></span>
</dt> <dd>

<span data-ttu-id="86665-112">Die Revisions Ebene der **nddebug-Info** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="86665-112">The revision level of the **NDDESHAREINFO** structure.</span></span> <span data-ttu-id="86665-113">Derzeit ist die Revisions Ebene 1.</span><span class="sxs-lookup"><span data-stu-id="86665-113">Currently, the revision level is 1.</span></span>

</dd> <dt>

<span data-ttu-id="86665-114">**lpszsharename**</span><span class="sxs-lookup"><span data-stu-id="86665-114">**lpszShareName**</span></span>
</dt> <dd>

<span data-ttu-id="86665-115">Der Name der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="86665-115">The name of the share.</span></span> <span data-ttu-id="86665-116">Diese Zeichenfolge darf nicht größer sein als die maximale Anzahl von \_ ndde ShareName-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="86665-116">This string must be no more than MAX\_NDDESHARENAME characters long.</span></span>

</dd> <dt>

<span data-ttu-id="86665-117">**lsharetype**</span><span class="sxs-lookup"><span data-stu-id="86665-117">**lShareType**</span></span>
</dt> <dd>

<span data-ttu-id="86665-118">Ein oder mehrere DDE-Freigabe Typen.</span><span class="sxs-lookup"><span data-stu-id="86665-118">One or more DDE share types.</span></span> <span data-ttu-id="86665-119">Dieser Member kann eine Kombination der folgenden unterstützten DDE-Freigabe Typen sein.</span><span class="sxs-lookup"><span data-stu-id="86665-119">This member can be a combination of the following supported DDE share types.</span></span>



| <span data-ttu-id="86665-120">Freigabetyp</span><span class="sxs-lookup"><span data-stu-id="86665-120">Share type</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="86665-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="86665-121">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <span data-ttu-id="86665-122"><dt>**Freigabe \_ \_Neuer**</dt> <dt>0x02</dt> eingeben</span><span class="sxs-lookup"><span data-stu-id="86665-122"><dt>**SHARE\_TYPE\_NEW**</dt> <dt>0x02</dt></span></span> </dl>          | <span data-ttu-id="86665-123">Die Freigabe enthält ein OLE-Anwendungs-/Topic-Paar.</span><span class="sxs-lookup"><span data-stu-id="86665-123">The share contains an OLE application/topic pair.</span></span><br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <span data-ttu-id="86665-124"><dt>**Freigabe \_ Geben Sie \_ Alter**</dt> <dt>0x01</dt> ein.</span><span class="sxs-lookup"><span data-stu-id="86665-124"><dt>**SHARE\_TYPE\_OLD**</dt> <dt>0x01</dt></span></span> </dl>          | <span data-ttu-id="86665-125">Die Freigabe enthält ein DDE-Anwendungs-/Topic-Paar.</span><span class="sxs-lookup"><span data-stu-id="86665-125">The share contains a DDE application/topic pair.</span></span><br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <span data-ttu-id="86665-126"><dt>**Freigabe \_ \_Typstatic**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="86665-126"><dt>**SHARE\_TYPE\_STATIC**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="86665-127">Die Freigabe enthält ein statisches Anwendungs-/Topic-Paar.</span><span class="sxs-lookup"><span data-stu-id="86665-127">The share contains a static application/topic pair.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="86665-128">**lpszapptopiclist**</span><span class="sxs-lookup"><span data-stu-id="86665-128">**lpszAppTopicList**</span></span>
</dt> <dd>

<span data-ttu-id="86665-129">Ein Zeiger auf einen Puffer, der NULL-terminierte Zeichen folgen für das DDE, OLE und statische Anwendungs-/Topic-Paare enthält.</span><span class="sxs-lookup"><span data-stu-id="86665-129">A pointer to a buffer containing null-terminated strings for the DDE, OLE, and static application/topic pairs.</span></span> <span data-ttu-id="86665-130">Der Puffer sollte das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="86665-130">The buffer should be in the following format:</span></span>

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

<span data-ttu-id="86665-131">**"ssharedflag"**</span><span class="sxs-lookup"><span data-stu-id="86665-131">**fSharedFlag**</span></span>
</dt> <dd>

<span data-ttu-id="86665-132">Wenn dieser Member **false** ist, lässt die DDE-Freigabe nicht zu, dass Remote Benutzer mithilfe von DDE kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="86665-132">If this member is **FALSE**, the DDE share will not allow remote users to communicate through it by using DDE.</span></span> <span data-ttu-id="86665-133">Lokale Benutzer können jedoch weiterhin über die DDE-Freigabe kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="86665-133">However, local users can still communicate through the DDE share.</span></span> <span data-ttu-id="86665-134">Lokale Client Links werden immer impliziert, wenn die zugehörige DACL Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="86665-134">Local client links are always implied if the associated DACL grants access.</span></span>

</dd> <dt>

<span data-ttu-id="86665-135">**Dienst**</span><span class="sxs-lookup"><span data-stu-id="86665-135">**fService**</span></span>
</dt> <dd>

<span data-ttu-id="86665-136">Wenn dieser Member festgelegt ist, überprüft die DDE-Freigabe nicht, ob der aktuelle Benutzer Sie als vertrauenswürdig festgelegt hat, bevor die DDE-Kommunikation zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="86665-136">If this member is set, the DDE share will not check whether the current user has set it as trusted before allowing DDE communication.</span></span>

</dd> <dt>

<span data-ttu-id="86665-137">**"sstartappflag"**</span><span class="sxs-lookup"><span data-stu-id="86665-137">**fStartAppFlag**</span></span>
</dt> <dd>

<span data-ttu-id="86665-138">Wenn dieser Member festgelegt ist und die Freigabe vertrauenswürdig ist, um Anwendungen zu starten, versucht NetDDE, die von **lpszapptopiclist** angegebene Anwendung zu starten, wenn er nicht anfänglich eine DDE-Konversation mit der Anwendung startet.</span><span class="sxs-lookup"><span data-stu-id="86665-138">If this member is set and the share is trusted to start applications, NetDDE will attempt to start the application specified by **lpszAppTopicList** if it cannot initially start a DDE conversation with the application.</span></span>

</dd> <dt>

<span data-ttu-id="86665-139">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="86665-139">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="86665-140">Wenn NetDDE eine Anwendung zum Initiieren einer DDE-Konversation startet, wird dieser Wert über den *nCmdShow* -Parameter der [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="86665-140">When NetDDE starts an application to initiate a DDE conversation, this value is sent to the application through the *nCmdShow* parameter of the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="86665-141">Es definiert den bevorzugten Modus, in dem das Anwendungsfenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86665-141">It defines the preferred mode for the application window to be shown in.</span></span> <span data-ttu-id="86665-142">Dieser Parameter ist nur dann von Bedeutung, wenn " **f startappflag** " aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="86665-142">This parameter is significant only if **fStartAppFlag** is active.</span></span> <span data-ttu-id="86665-143">Der angemeldete Benutzer, in dessen Kontext die Anwendung gestartet wurde, kann diese Option auch überschreiben, wenn die Freigabe zum vertrauenswürdigen Status herauf gestuft wird.</span><span class="sxs-lookup"><span data-stu-id="86665-143">The logged on user in whose context the application is started can also override this option when promoting the share to trusted status.</span></span> <span data-ttu-id="86665-144">Der Standardwert für diesen Member ist "SW \_ showmaximized".</span><span class="sxs-lookup"><span data-stu-id="86665-144">The default for this member is SW\_SHOWMAXIMIZED.</span></span>

</dd> <dt>

<span data-ttu-id="86665-145">**qmodifyid**</span><span class="sxs-lookup"><span data-stu-id="86665-145">**qModifyId**</span></span>
</dt> <dd>

<span data-ttu-id="86665-146">Eine 8-Byte-Seriennummer, die die Änderungs Seriennummer der DDE-Freigabe angibt.</span><span class="sxs-lookup"><span data-stu-id="86665-146">An 8-byte serial number that indicates the modification serial number of the DDE share.</span></span> <span data-ttu-id="86665-147">Jedes Mal, wenn die DDE-Freigabe durch einen [**nddesharesetinfo**](nddesharesetinfo.md) -oder einen [**nddesetsharesecurity**](nddesetsharesecurity.md) -Aufruf geändert wird, werden diese Werte geändert.</span><span class="sxs-lookup"><span data-stu-id="86665-147">Every time the DDE share is modified by a [**NDdeShareSetInfo**](nddesharesetinfo.md) or [**NDdeSetShareSecurity**](nddesetsharesecurity.md) call, these values are changed.</span></span>

</dd> <dt>

<span data-ttu-id="86665-148">**cnumitems**</span><span class="sxs-lookup"><span data-stu-id="86665-148">**cNumItems**</span></span>
</dt> <dd>

<span data-ttu-id="86665-149">Die Anzahl der in **lpszitemlist** aufgeführten Elemente.</span><span class="sxs-lookup"><span data-stu-id="86665-149">The number of items listed in **lpszItemList**.</span></span> <span data-ttu-id="86665-150">Wenn **cnumitems** gleich 0 (null) ist, ist **lpszitemlist** leer, und die Freigabe Informationen und die zugehörige Sicherheits Beschreibung gelten für alle Elemente, die von der zugehörigen Anwendung bedient werden.</span><span class="sxs-lookup"><span data-stu-id="86665-150">If **cNumItems** is zero, then **lpszItemList** is empty, and the share information and associated security descriptor apply to all items serviced by the associated application.</span></span>

</dd> <dt>

<span data-ttu-id="86665-151">**lpszitemlist**</span><span class="sxs-lookup"><span data-stu-id="86665-151">**lpszItemList**</span></span>
</dt> <dd>

<span data-ttu-id="86665-152">Ein Zeiger auf einen Puffer mit null-terminierten Zeichen folgen, die die Elemente angeben, die von der Client Anwendung in einer DDE-Transaktion angefordert oder gestartet werden können.</span><span class="sxs-lookup"><span data-stu-id="86665-152">A pointer to a buffer containing null-terminated strings that specify the items the client application in a DDE transaction can request or start advise loops on.</span></span> <span data-ttu-id="86665-153">Wenn keine Elemente aufgelistet werden, kann die DDE-Freigabe alle Elemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="86665-153">If no items are listed, the DDE share allows any item to be used.</span></span> <span data-ttu-id="86665-154">Die Anzahl der Elemente in der Liste muss der Anzahl der **cnumitems** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="86665-154">The number of items in the list must match the **cNumItems** count.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86665-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86665-155">Requirements</span></span>



| <span data-ttu-id="86665-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86665-156">Requirement</span></span> | <span data-ttu-id="86665-157">Wert</span><span class="sxs-lookup"><span data-stu-id="86665-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="86665-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86665-158">Minimum supported client</span></span><br/> | <span data-ttu-id="86665-159">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86665-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="86665-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86665-160">Minimum supported server</span></span><br/> | <span data-ttu-id="86665-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86665-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="86665-162">Header</span><span class="sxs-lookup"><span data-stu-id="86665-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="86665-163"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="86665-163"><dt>Nddeapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86665-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86665-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86665-165">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="86665-165">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="86665-166">Netzwerk-DDE-Strukturen</span><span class="sxs-lookup"><span data-stu-id="86665-166">Network DDE Structures</span></span>](network-dde-structures.md)
</dt> <dt>

[<span data-ttu-id="86665-167">**Ndde setsharesecurity**</span><span class="sxs-lookup"><span data-stu-id="86665-167">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> <dt>

[<span data-ttu-id="86665-168">**Nddesharesetinfo**</span><span class="sxs-lookup"><span data-stu-id="86665-168">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> <dt>

[<span data-ttu-id="86665-169">**WinMain**</span><span class="sxs-lookup"><span data-stu-id="86665-169">**WinMain**</span></span>](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

