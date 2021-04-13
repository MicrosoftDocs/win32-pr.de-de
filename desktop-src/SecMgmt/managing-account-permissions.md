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
# <a name="managing-account-permissions"></a>Verwalten von Konto Berechtigungen

Die LSA bietet verschiedene Funktionen, die von Anwendungen aufgerufen werden können, um [*Berechtigungen*](/windows/desktop/SecGloss/p-gly) für Benutzer-, Gruppen-und lokale Gruppenkonten aufzulisten oder festzulegen.

Bevor Sie Kontoinformationen verwalten können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)gezeigt. Außerdem müssen Sie zum Auflisten oder Bearbeiten von Berechtigungen für ein Konto über die [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) für das Konto verfügen. Die Anwendung kann eine SID anhand des Konto namens finden, wie unter über [Setzung zwischen Namen und SIDs](translating-between-names-and-sids.md)beschrieben.

Für den Zugriff auf alle Konten, die über eine bestimmte Berechtigung verfügen, können Sie [**lsaenumerateaccountswithuserright**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)aufrufen. Diese Funktion füllt ein Array mit den SIDs aller Konten mit der angegebenen Berechtigung auf.

Nachdem Sie die SID eines Kontos abgerufen haben, können Sie die zugehörigen Berechtigungen ändern. Wenden Sie [**lsaaddaccounumghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) an, um dem Konto Berechtigungen hinzuzufügen. Wenn das angegebene Konto nicht vorhanden ist, wird es von **lsaaddaccountrghts** erstellt. Um Berechtigungen von einem Konto zu entfernen, nennen Sie [**lsaremuveaccounschghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights). Wenn Sie alle Berechtigungen aus einem Konto entfernen, löscht **lsareporveaccountrips** auch das Konto.

Die Anwendung kann die derzeit einem Konto zugewiesenen Berechtigungen überprüfen, indem Sie [**lsaenumerateaccountrghts**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)aufrufen. Diese Funktion füllt ein Array von [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Strukturen auf. Jede Struktur enthält den Namen einer Berechtigung, die vom angegebenen Konto gehalten wird.

Im folgenden Beispiel wird einem Konto die SeServiceLogonRight-Berechtigung hinzugefügt. In diesem Beispiel gibt die AccountSid-Variable die SID des Kontos an. Weitere Informationen zur Suche nach einer Konto-SID finden Sie unter über [setzen zwischen Namen und SIDs](translating-between-names-and-sids.md).


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



Im vorherigen Beispiel konvertiert die Funktion initlsastring eine [*Unicode*](/windows/desktop/SecGloss/u-gly) -Zeichenfolge in eine [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur. Der Code für diese Funktion wird in [Verwenden von LSA-Unicode](using-lsa-unicode-strings.md)-Zeichen folgen angezeigt.

 

 
