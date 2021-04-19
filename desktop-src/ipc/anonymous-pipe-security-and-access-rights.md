---
description: Sie können eine Sicherheits Beschreibung für eine anonyme Pipe angeben, wenn Sie die Funktion "-Funktion" aufrufen. Die Sicherheits Beschreibung steuert den Zugriff auf die Lese-und schreibenden der Pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Sicherheit und Zugriffsrechte für anonyme Pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350119"
---
# <a name="anonymous-pipe-security-and-access-rights"></a><span data-ttu-id="23c62-104">Sicherheit und Zugriffsrechte für anonyme Pipe</span><span class="sxs-lookup"><span data-stu-id="23c62-104">Anonymous Pipe Security and Access Rights</span></span>

<span data-ttu-id="23c62-105">Mithilfe der Windows-Sicherheit können Sie den Zugriff auf anonyme Pipes steuern.</span><span class="sxs-lookup"><span data-stu-id="23c62-105">Windows security enables you to control access to anonymous pipes.</span></span> <span data-ttu-id="23c62-106">Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="23c62-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="23c62-107">Sie können eine [Sicherheits Beschreibung](/windows/desktop/SecAuthZ/security-descriptors) für eine Pipe angeben, wenn [**Sie die Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) "-Funktion" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="23c62-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a pipe when you call the [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function.</span></span> <span data-ttu-id="23c62-108">Die Sicherheits Beschreibung steuert den Zugriff auf die Lese-und schreibenden der Pipe.</span><span class="sxs-lookup"><span data-stu-id="23c62-108">The security descriptor controls access to both the read and write ends of the pipe.</span></span> <span data-ttu-id="23c62-109">Wenn Sie **null** angeben, erhält die Pipe eine Standard Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="23c62-109">If you specify **NULL**, the pipe gets a default security descriptor.</span></span> <span data-ttu-id="23c62-110">Die ACLs in der Standard Sicherheits Beschreibung für eine Pipe stammen aus dem primären Token oder dem Identitätswechsel Token des Erstellers.</span><span class="sxs-lookup"><span data-stu-id="23c62-110">The ACLs in the default security descriptor for a pipe come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="23c62-111">Um die Sicherheits Beschreibung eines Pipe abzurufen, rufen Sie die [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="23c62-111">To retrieve a pipe's security descriptor, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span> <span data-ttu-id="23c62-112">Um die Sicherheits Beschreibung einer Pipe zu ändern, müssen Sie die Funktion [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="23c62-112">To change a pipe's security descriptor, call the [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) function.</span></span>

<span data-ttu-id="23c62-113">Die Funktion " [**kreatepipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) " gibt zwei Handles an die anonyme Pipe zurück: ein Lese Handle mit generischem \_ Lese-und Synchronisierungs Zugriff und ein Schreib Handle mit generischem \_ Schreib-und Synchronisierungs Zugriff.</span><span class="sxs-lookup"><span data-stu-id="23c62-113">The [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function returns two handles to the anonymous pipe: a read handle with GENERIC\_READ and SYNCHRONIZE access; and a write handle with GENERIC\_WRITE and SYNCHRONIZE access.</span></span> <span data-ttu-id="23c62-114">\_Für den generischen Lesezugriff und den generischen \_ Schreibzugriff wird dieselbe Zugriffsrechte Zuordnung wie für Named Pipes verwendet.</span><span class="sxs-lookup"><span data-stu-id="23c62-114">GENERIC\_READ and GENERIC\_WRITE access use the same access rights mapping as for named pipes.</span></span>

<span data-ttu-id="23c62-115">Der generische \_ Lesezugriff für eine anonyme Pipe kombiniert die Rechte zum Lesen von Daten aus der Pipe, zum Lesen von Pipe-Attributen, zum Lesen erweiterter Attribute und zum Lesen der DACL der Pipe.</span><span class="sxs-lookup"><span data-stu-id="23c62-115">GENERIC\_READ access for an anonymous pipe combines the rights to read data from the pipe, read pipe attributes, read extended attributes, and read the pipe's DACL.</span></span>

<span data-ttu-id="23c62-116">\_Der generische Schreibzugriff für eine anonyme Pipe kombiniert die Rechte zum Schreiben von Daten in die Pipe, zum Anfügen von Daten an die Pipe, zum Schreiben von Pipe-Attributen, zum Schreiben erweiterter Attribute und zum Lesen der DACL der Pipe.</span><span class="sxs-lookup"><span data-stu-id="23c62-116">GENERIC\_WRITE access for an anonymous pipe combines the rights to write data to the pipe, append data to it, write pipe attributes, write extended attributes, and read the pipe's DACL.</span></span>

 

 
