---
description: Die LSA-Richtlinie stellt zwei Funktionen bereit, mit denen Sie private Daten festlegen und abrufen können.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Speichern privater Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393498"
---
# <a name="storing-private-data"></a>Speichern privater Daten

Die LSA-Richtlinie stellt zwei Funktionen bereit, mit denen Sie private Daten festlegen und abrufen können. Diese Daten werden als verschlüsselte Zeichenfolge in der Registrierung gespeichert. Beispielsweise können Sie diese Funktionen zum Speichern von Server Konto Kennwörtern und anderen vertraulichen Informationen verwenden.

Ruft die [**lsastoreprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion auf, um private Daten zu speichern und zu verschlüsseln. Wie im [privaten Datenobjekt](private-data-object.md)beschrieben, beinhalten private Datenobjekte drei spezialisierte Typen: "local", "Global" und "Machine". Fügen Sie zum Erstellen eines spezialisierten Objekts dem an **lsastoreprivatedata** weiter gegebenen Schlüsselnamen ein Präfix hinzu: "L $" für lokale Objekte, "G $" für globale Objekte und "M $" für Computer Objekte. Wenn Sie keinen dieser speziellen Typen erstellen, müssen Sie kein Schlüsselnamen Präfix angeben.

Um zuvor gespeicherte Private Daten abzurufen und zu decodieren, rufen Sie [**lsarelteveprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)auf. Beachten Sie, dass Sie keine privaten Computer Datenobjekte abrufen können. Computer Objekte können nur vom Betriebssystem abgerufen werden.

Bevor Sie private Daten speichern oder abrufen können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)veranschaulicht.

Im folgenden Beispiel wird ein lokales privates Datenobjekt erstellt. Beachten Sie, dass die Funktion initlsastring eine [*Unicode*](/windows/desktop/SecGloss/u-gly) -Zeichenfolge in eine [**LSA-Unicode- \_ \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur konvertiert. Der Code für diese Funktion wird in [Verwenden von LSA-Unicode](using-lsa-unicode-strings.md)-Zeichen folgen angezeigt.


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> Die von der [**lsastoreprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion gespeicherten Daten sind nicht absolut geschützt. Der Schlüssel verfügt jedoch über eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL), mit der nur die Ersteller und Administratoren die Daten lesen können.

 

 

 
