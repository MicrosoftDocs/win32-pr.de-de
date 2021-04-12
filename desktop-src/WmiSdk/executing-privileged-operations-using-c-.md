---
description: Spezielle Client Anwendungen rufen möglicherweise privilegierte Vorgänge auf.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Ausführen privilegierter Vorgänge mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344918"
---
# <a name="executing-privileged-operations-using-c"></a><span data-ttu-id="dbeeb-103">Ausführen privilegierter Vorgänge mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="dbeeb-103">Executing Privileged Operations Using C++</span></span>

<span data-ttu-id="dbeeb-104">Spezielle Client Anwendungen rufen möglicherweise privilegierte Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-104">Special client applications might invoke privileged operations.</span></span> <span data-ttu-id="dbeeb-105">Beispielsweise könnte eine Anwendung einem Vorgesetzten einen Neustart eines nicht reagierenden Office-Computers ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-105">For example, an application could allow a manager to reboot an unresponsive office computer.</span></span> <span data-ttu-id="dbeeb-106">Mithilfe von Windows-Verwaltungsinstrumentation (WMI) können Sie einen privilegierten Vorgang ausführen, indem Sie den WMI-Anbieter für den privilegierten Vorgang aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-106">By using Windows Management Instrumentation (WMI), you can execute a privileged operation by calling the WMI provider for the privileged operation.</span></span>

<span data-ttu-id="dbeeb-107">Im folgenden Verfahren wird beschrieben, wie ein Anbieter für einen privilegierten Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-107">The following procedure describes how to call a provider for a privileged operation.</span></span>

<span data-ttu-id="dbeeb-108">**So fordern Sie einen Anbieter für einen privilegierten Vorgang an**</span><span class="sxs-lookup"><span data-stu-id="dbeeb-108">**To call a provider for a privileged operation**</span></span>

1.  <span data-ttu-id="dbeeb-109">Rufen Sie die Berechtigungen für den Client Prozess ab, um den privilegierten Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-109">Obtain permissions for the client process to execute the privileged operation.</span></span>

    <span data-ttu-id="dbeeb-110">In der Regel legt ein Administrator die Berechtigungen mithilfe von System Verwaltungs Tools fest – vor der Ausführung des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-110">Typically, an administrator sets the permissions using system administrative tools—prior to running the process.</span></span>

2.  <span data-ttu-id="dbeeb-111">Abrufen der Berechtigung für den Anbieter Prozess zum Aktivieren des privilegierten Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-111">Obtain permission for the provider process to enable the privileged operation.</span></span>

    <span data-ttu-id="dbeeb-112">In der Regel können Sie Anbieter Berechtigungen mithilfe eines Aufrufes der Funktion "- [**tokenprivilegien**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-112">Typically, you can set provider permissions with a call to the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>

3.  <span data-ttu-id="dbeeb-113">Abrufen der Berechtigung für den Client Prozess zum Aktivieren des privilegierten Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-113">Obtain permission for the client process to enable the privileged operation.</span></span>

    <span data-ttu-id="dbeeb-114">Dieser Schritt ist nur erforderlich, wenn der Anbieter für den Client lokal ist.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-114">This step is necessary only if the provider is local to the client.</span></span> <span data-ttu-id="dbeeb-115">Wenn der Client und der Anbieter auf demselben Computer vorhanden sind, muss der Client den privilegierten Vorgang mithilfe einer der folgenden Verfahren explizit aktivieren:</span><span class="sxs-lookup"><span data-stu-id="dbeeb-115">If the client and provider exist on the same computer, the client must specifically enable the privileged operation by using one of the following techniques:</span></span>

    -   <span data-ttu-id="dbeeb-116">Wenn der Client den Prozess besitzt, kann der Client " [**anpasstokenprivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " verwenden, um das Prozess Token vor dem Aufrufen von WMI anzupassen.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-116">If the client owns the process, the client can use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to adjust the process token before calling WMI.</span></span> <span data-ttu-id="dbeeb-117">In diesem Fall müssen Sie keine weiteren Codes programmieren.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-117">In this case, you do not need to code any further.</span></span>
    -   <span data-ttu-id="dbeeb-118">Wenn der Client nicht auf das Client Token zugreifen kann, kann der Client das folgende Verfahren zum Erstellen eines Thread Tokens und zum Verwenden von "- [**tokenprivilegien**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " für dieses Token verwenden.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-118">If the client cannot access the client token, the client can use the following procedure to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="dbeeb-119">Im folgenden Verfahren wird das Erstellen eines Thread Tokens und [**das Verwenden von**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) "" für dieses Token beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-119">The following procedure describes how to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="dbeeb-120">**So erstellen Sie ein Thread Token und verwenden "resoltokenprivileges" für dieses Token**</span><span class="sxs-lookup"><span data-stu-id="dbeeb-120">**To create a thread token and use AdjustTokenPrivileges on that token**</span></span>

1.  <span data-ttu-id="dbeeb-121">Erstellen Sie eine Kopie des Prozess Tokens [**durch Aufrufen von**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself)Identitätsnachweis.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-121">Create a copy of the process token by calling [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span></span>
2.  <span data-ttu-id="dbeeb-122">Abrufen des neu erstellten Thread Tokens durch Aufrufen von [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span><span class="sxs-lookup"><span data-stu-id="dbeeb-122">Retrieve the newly created thread token by calling [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span></span>
3.  <span data-ttu-id="dbeeb-123">Aktivieren Sie den privilegierten Vorgang mit einem [**calltokenprivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) -Befehl für das neue Token.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-123">Enable the privileged operation with a call to [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on the new token.</span></span>
4.  <span data-ttu-id="dbeeb-124">Rufen Sie einen Zeiger auf [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)ab.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-124">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>
5.  <span data-ttu-id="dbeeb-125">Verdecken Sie den Zeiger mit " [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) " durch einen Aufrufen von " [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)".</span><span class="sxs-lookup"><span data-stu-id="dbeeb-125">Cloak the pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>
6.  <span data-ttu-id="dbeeb-126">Wiederholen Sie die Schritte 1 bis 5 für jeden WMI-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-126">Repeat steps 1 through 5 on each call to WMI.</span></span>

    > [!Note]  
    > <span data-ttu-id="dbeeb-127">Sie müssen die Schritte wiederholen, weil com Token falsch zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-127">You must repeat the steps because COM caches tokens incorrectly.</span></span>

     

<span data-ttu-id="dbeeb-128">Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-128">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="dbeeb-129">Im folgenden Codebeispiel wird gezeigt, wie Berechtigungen auf einem lokalen Computer aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="dbeeb-129">The following code example shows how to enable privileges on a local machine.</span></span>


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
