---
title: Software Anforderungen für die WinSNMP-API
description: Eine WinSNMP-Anwendung muss über die Dynamic Link Library-WSNMP32.DLL auf die WinSNMP-API zugreifen.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206232"
---
# <a name="software-requirements-for-the-winsnmp-api"></a><span data-ttu-id="6c39d-103">Software Anforderungen für die WinSNMP-API</span><span class="sxs-lookup"><span data-stu-id="6c39d-103">Software Requirements for the WinSNMP API</span></span>

<span data-ttu-id="6c39d-104">Eine WinSNMP-Anwendung muss über die Dynamic Link Library-WSNMP32.DLL auf die WinSNMP-API zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6c39d-104">A WinSNMP application must access the WinSNMP API through the dynamic-link library WSNMP32.DLL.</span></span>

<span data-ttu-id="6c39d-105">Die folgenden Dateien sind erforderlich, um die Funktionalität der WinSNMP-API zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6c39d-105">The following files are required to support the functionality of the WinSNMP API.</span></span>



| <span data-ttu-id="6c39d-106">Dateiname</span><span class="sxs-lookup"><span data-stu-id="6c39d-106">Filename</span></span>     | <span data-ttu-id="6c39d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c39d-107">Description</span></span>                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c39d-108">WSNMP32. LIB</span><span class="sxs-lookup"><span data-stu-id="6c39d-108">WSNMP32.LIB</span></span>  | <span data-ttu-id="6c39d-109">WinSNMP-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c39d-109">WinSNMP Library</span></span>                                                                              |
| <span data-ttu-id="6c39d-110">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="6c39d-110">WSNMP32.DLL</span></span>  | <span data-ttu-id="6c39d-111">Stellt WinSNMP-Schnittstelle bereit</span><span class="sxs-lookup"><span data-stu-id="6c39d-111">Provides WinSNMP interface</span></span>                                                                   |
| <span data-ttu-id="6c39d-112">Winsnmp. Micha</span><span class="sxs-lookup"><span data-stu-id="6c39d-112">WINSNMP.H</span></span>    | <span data-ttu-id="6c39d-113">WinSNMP-Header Datei</span><span class="sxs-lookup"><span data-stu-id="6c39d-113">WinSNMP header file</span></span>                                                                          |
| <span data-ttu-id="6c39d-114">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="6c39d-114">SNMPTRAP.EXE</span></span> | <span data-ttu-id="6c39d-115">Empfängt SNMP-Traps und leitet Sie an MGMTAPI.DLL, die Microsoft SNMP Manager-API-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="6c39d-115">Receives SNMP traps and forwards them to MGMTAPI.DLL, the Microsoft SNMP Manager API library</span></span> |
| <span data-ttu-id="6c39d-116">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="6c39d-116">SNMPAPI.DLL</span></span>  | <span data-ttu-id="6c39d-117">Stellt SNMP-Hilfsprogramme bereit</span><span class="sxs-lookup"><span data-stu-id="6c39d-117">Provides SNMP utilities</span></span>                                                                      |



 

 

 




