---
description: In diesem Abschnitt werden die Makros des Windows Shell-Hilfsprogramms beschrieben.
title: Shellmakros
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960002"
---
# <a name="shell-macros"></a><span data-ttu-id="a0e4a-103">Shellmakros</span><span class="sxs-lookup"><span data-stu-id="a0e4a-103">Shell Macros</span></span>

<span data-ttu-id="a0e4a-104">In diesem Abschnitt werden die Makros des Windows Shell-Hilfsprogramms beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-104">This section describes the Windows Shell utility macros.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a0e4a-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a0e4a-105">In this section</span></span>



| <span data-ttu-id="a0e4a-106">Thema</span><span class="sxs-lookup"><span data-stu-id="a0e4a-106">Topic</span></span>                                                                  | <span data-ttu-id="a0e4a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0e4a-107">Description</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0e4a-108">**\_PropertyKey definieren**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-108">**DEFINE\_PROPERTYKEY**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | <span data-ttu-id="a0e4a-109">Wird zum Packen eines Format Bezeichners (fmtid) und eines Eigenschafts Bezeichners (PID) in eine [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) -Struktur verwendet, die einen Eigenschafts Schlüssel darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-109">Used to pack a format identifier (FMTID) and property identifier (PID) into a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure that represents a property key.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a0e4a-110">**IID \_ PPV-Argumente \_**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-110">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | <span data-ttu-id="a0e4a-111">Wird zum Abrufen eines Schnittstellen Zeigers verwendet. dabei wird der IID-Wert der angeforderten Schnittstelle automatisch basierend auf dem Typ des verwendeten Schnittstellen Zeigers bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-111">Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used.</span></span> <span data-ttu-id="a0e4a-112">Dadurch wird ein allgemeiner Codierungsfehler vermieden, indem der zum Zeitpunkt der Kompilierung übergebenen Wert überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-112">This avoids a common coding error by checking the type of the value passed at compile time.</span></span><br/> |
| [<span data-ttu-id="a0e4a-113">**Isequalpropertykey**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-113">**IsEqualPropertyKey**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | <span data-ttu-id="a0e4a-114">Vergleicht die Member zweier [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) -Strukturen und gibt zurück, ob Sie gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-114">Compares the members of two [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structures and returns whether they are equal.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="a0e4a-115">**Makedllverull**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-115">**MAKEDLLVERULL**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | <span data-ttu-id="a0e4a-116">Wird verwendet, um dll-Versionsinformationen in einen ULONGLONG-Wert zu packen.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-116">Used to pack DLL version information into a ULONGLONG value.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="a0e4a-117">**NETADDR \_ displayerrortip**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-117">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | <span data-ttu-id="a0e4a-118">Zeigt eine Fehlermeldung in der Sprechblasen Info an, die dem Netzwerk Adress Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-118">Displays an error message in the balloon tip associated with the network address control.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="a0e4a-119">**NETADDR- \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-119">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | <span data-ttu-id="a0e4a-120">Gibt an, ob eine Netzwerkadresse einem angegebenen Typ und Format entspricht.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-120">Indicates whether a network address conforms to a specified type and format.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="a0e4a-121">**NETADDR- \_ getallowtype**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-121">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | <span data-ttu-id="a0e4a-122">Ruft die Netzwerk Adresstypen ab, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-122">Retrieves the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="a0e4a-123">**NETADDR- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="a0e4a-123">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | <span data-ttu-id="a0e4a-124">Legt die Netzwerk Adresstypen fest, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0e4a-124">Sets the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                     |



 

 

 
