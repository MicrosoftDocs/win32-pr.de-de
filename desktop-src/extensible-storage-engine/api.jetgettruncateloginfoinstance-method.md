---
description: Weitere Informationen finden Sie in der API. jetgettruneureloginfoinstance-Methode.
title: API. jetgettruneureloginfoinstance-Methode
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218471"
---
# <a name="apijetgettruncateloginfoinstance-method"></a><span data-ttu-id="95b04-103">API. jetgettruneureloginfoinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="95b04-103">Api.JetGetTruncateLogInfoInstance method</span></span>

<span data-ttu-id="95b04-104">Wird bei einer von [jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE beginexternalbackupgrbit)](./api.jetbeginexternalbackupinstance-method.md) verwendet, um eine Instanz nach den Namen der Transaktionsprotokoll Dateien abzufragen, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="95b04-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="95b04-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95b04-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="95b04-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95b04-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95b04-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b04-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="95b04-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95b04-108">Parameters</span></span>

  - <span data-ttu-id="95b04-109">instance</span><span class="sxs-lookup"><span data-stu-id="95b04-109">instance</span></span>  
    <span data-ttu-id="95b04-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95b04-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="95b04-111">Die-Instanz, für die die Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="95b04-111">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="95b04-112">files</span><span class="sxs-lookup"><span data-stu-id="95b04-112">files</span></span>  
    <span data-ttu-id="95b04-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="95b04-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="95b04-114">Gibt eine Liste von null-terminierten Zeichen folgen zurück, die den Satz von Daten Bank Protokolldateien beschreiben, die nach Abschluss der Sicherung sicher gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="95b04-114">Returns a list of null terminated strings describing the set of database log files that can be safely deleted after the backup completes.</span></span> <span data-ttu-id="95b04-115">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="95b04-115">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="95b04-116">Jede NULL terminierte Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="95b04-116">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="95b04-117">maxChars</span><span class="sxs-lookup"><span data-stu-id="95b04-117">maxChars</span></span>  
    <span data-ttu-id="95b04-118">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="95b04-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="95b04-119">Maximale Anzahl der abzurufenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="95b04-119">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="95b04-120">actualchars</span><span class="sxs-lookup"><span data-stu-id="95b04-120">actualChars</span></span>  
    <span data-ttu-id="95b04-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="95b04-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="95b04-122">Die tatsächliche Größe der Datei Liste.</span><span class="sxs-lookup"><span data-stu-id="95b04-122">Actual size of the file list.</span></span> <span data-ttu-id="95b04-123">Wenn dieser Wert größer als maxChars ist, wurde die Liste abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="95b04-123">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="95b04-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95b04-124">Remarks</span></span>

<span data-ttu-id="95b04-125">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="95b04-125">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="95b04-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b04-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95b04-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="95b04-127">Reference</span></span>

[<span data-ttu-id="95b04-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="95b04-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="95b04-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="95b04-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="95b04-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="95b04-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
