---
description: Die LSA bietet verschiedene Funktionen, die von Anwendungen aufgerufen werden können, um Berechtigungen für Benutzer-, Gruppen-und lokale Gruppenkonten aufzulisten oder festzulegen.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Verwalten von Konto Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484587"
---
# <a name="managing-account-permissions"></a><span data-ttu-id="195e2-103">Verwalten von Konto Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="195e2-103">Managing Account Permissions</span></span>

<span data-ttu-id="195e2-104">Die LSA bietet verschiedene Funktionen, die von Anwendungen aufgerufen werden können, um [*Berechtigungen*](/windows/desktop/SecGloss/p-gly) für Benutzer-, Gruppen-und lokale Gruppenkonten aufzulisten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="195e2-104">The LSA provides several functions that applications can call to enumerate or set [*privileges*](/windows/desktop/SecGloss/p-gly) for user, group, and local group accounts.</span></span>

<span data-ttu-id="195e2-105">Bevor Sie Kontoinformationen verwalten können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="195e2-105">Before you can manage account information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="195e2-106">Außerdem müssen Sie zum Auflisten oder Bearbeiten von Berechtigungen für ein Konto über die [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) für das Konto verfügen.</span><span class="sxs-lookup"><span data-stu-id="195e2-106">In addition, to enumerate or edit permissions for an account, you must have the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) for that account.</span></span> <span data-ttu-id="195e2-107">Die Anwendung kann eine SID anhand des Konto namens finden, wie unter über [Setzung zwischen Namen und SIDs](translating-between-names-and-sids.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="195e2-107">Your application can locate a SID given the account name, as described in [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>

<span data-ttu-id="195e2-108">Für den Zugriff auf alle Konten, die über eine bestimmte Berechtigung verfügen, können Sie [**lsaenumerateaccountswithuserright**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="195e2-108">To access all accounts that have a particular permission, call [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span></span> <span data-ttu-id="195e2-109">Diese Funktion füllt ein Array mit den SIDs aller Konten mit der angegebenen Berechtigung auf.</span><span class="sxs-lookup"><span data-stu-id="195e2-109">This function populates an array with the SIDs of all accounts that have the specified permission.</span></span>

<span data-ttu-id="195e2-110">Nachdem Sie die SID eines Kontos abgerufen haben, können Sie die zugehörigen Berechtigungen ändern.</span><span class="sxs-lookup"><span data-stu-id="195e2-110">After you have obtained the SID of an account, you can modify its permissions.</span></span> <span data-ttu-id="195e2-111">Wenden Sie [**lsaaddaccounumghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) an, um dem Konto Berechtigungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="195e2-111">Call [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) to add permissions to the account.</span></span> <span data-ttu-id="195e2-112">Wenn das angegebene Konto nicht vorhanden ist, wird es von **lsaaddaccountrghts** erstellt.</span><span class="sxs-lookup"><span data-stu-id="195e2-112">If the specified account does not exist, **LsaAddAccountRights** creates it.</span></span> <span data-ttu-id="195e2-113">Um Berechtigungen von einem Konto zu entfernen, nennen Sie [**lsaremuveaccounschghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span><span class="sxs-lookup"><span data-stu-id="195e2-113">To remove permissions from an account, call [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span></span> <span data-ttu-id="195e2-114">Wenn Sie alle Berechtigungen aus einem Konto entfernen, löscht **lsareporveaccountrips** auch das Konto.</span><span class="sxs-lookup"><span data-stu-id="195e2-114">If you remove all permissions from an account, **LsaRemoveAccountRights** also deletes the account.</span></span>

<span data-ttu-id="195e2-115">Die Anwendung kann die derzeit einem Konto zugewiesenen Berechtigungen überprüfen, indem Sie [**lsaenumerateaccountrghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="195e2-115">Your application can check the permissions currently assigned to an account by calling [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span></span> <span data-ttu-id="195e2-116">Diese Funktion füllt ein Array von [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Strukturen auf.</span><span class="sxs-lookup"><span data-stu-id="195e2-116">This function populates an array of [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures.</span></span> <span data-ttu-id="195e2-117">Jede Struktur enthält den Namen einer Berechtigung, die vom angegebenen Konto gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="195e2-117">Each structure contains the name of a privilege held by the specified account.</span></span>

<span data-ttu-id="195e2-118">Im folgenden Beispiel wird einem Konto die SeServiceLogonRight-Berechtigung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="195e2-118">The following example adds the SeServiceLogonRight permission to an account.</span></span> <span data-ttu-id="195e2-119">In diesem Beispiel gibt die AccountSid-Variable die SID des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="195e2-119">In this example, the AccountSID variable specifies the SID of the account.</span></span> <span data-ttu-id="195e2-120">Weitere Informationen zur Suche nach einer Konto-SID finden Sie unter über [setzen zwischen Namen und SIDs](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="195e2-120">For more information about how to lookup an account SID, see [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



<span data-ttu-id="195e2-121">Im vorherigen Beispiel konvertiert die Funktion initlsastring eine [*Unicode*](/windows/desktop/SecGloss/u-gly) -Zeichenfolge in eine [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur.</span><span class="sxs-lookup"><span data-stu-id="195e2-121">In the preceding example, the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="195e2-122">Der Code für diese Funktion wird in [Verwenden von LSA-Unicode](using-lsa-unicode-strings.md)-Zeichen folgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="195e2-122">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

 

 
