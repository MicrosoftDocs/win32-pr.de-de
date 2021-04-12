---
description: Im folgenden Beispiel wird eine Zertifikat Speicher Eigenschaft, der lokalisierte Speicher Name, festgelegt und abgerufen. Diese Eigenschaft wird nicht beibehalten, wenn der Speicher geschlossen wird.
ms.assetid: 9fb368c9-a0d7-4c5f-9a38-7ef8f7283354
title: 'Beispiel-C-Programm: festlegen und erhalten von Zertifikat Speicher Eigenschaften'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7337027c265376f9145ef7b68f359250223d20f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345748"
---
# <a name="example-c-program-setting-and-getting-certificate-store-properties"></a><span data-ttu-id="b971f-104">Beispiel-C-Programm: festlegen und erhalten von Zertifikat Speicher Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b971f-104">Example C Program: Setting and Getting Certificate Store Properties</span></span>

<span data-ttu-id="b971f-105">Im folgenden Beispiel wird eine Zertifikat Speicher Eigenschaft, der lokalisierte Speicher Name, festgelegt und abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b971f-105">The following example sets and gets a certificate store property, the localized store name.</span></span> <span data-ttu-id="b971f-106">Diese Eigenschaft wird nicht beibehalten, wenn der Speicher geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b971f-106">This property is not persisted when the store is closed.</span></span>

<span data-ttu-id="b971f-107">In diesem Beispiel werden die folgenden Aufgaben und [*kryptoapi*](../secgloss/c-gly.md) -Funktionen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b971f-107">This example illustrates the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="b971f-108">Öffnen eines Zertifikat Speicher mithilfe von " [**certopeinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)".</span><span class="sxs-lookup"><span data-stu-id="b971f-108">Opening a certificate store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="b971f-109">Festlegen des lokalisierten Namens des Stores mithilfe von " [**certsetstoreproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)".</span><span class="sxs-lookup"><span data-stu-id="b971f-109">Setting the localized name of the store using [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty).</span></span>
-   <span data-ttu-id="b971f-110">Abrufen des lokalisierten Namens des Stores mithilfe von " [**certgetstoreproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)".</span><span class="sxs-lookup"><span data-stu-id="b971f-110">Retrieving the localized name of the store using [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty).</span></span>
-   <span data-ttu-id="b971f-111">Der vordefinierte lokalisierte Speicher Name wird mithilfe von " [**cryptfindlocalizedname**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname)" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b971f-111">Retrieving the predefined localized store name using [**CryptFindLocalizedName**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname).</span></span>
-   <span data-ttu-id="b971f-112">Speichern Sie den Zertifikat Speicher als [*PKCS \# 7*](../secgloss/p-gly.md) -Nachricht in einer Datei mit [**certsavestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore).</span><span class="sxs-lookup"><span data-stu-id="b971f-112">Save the certificate store as a [*PKCS \#7*](../secgloss/p-gly.md) message to a file using [**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore).</span></span>
-   <span data-ttu-id="b971f-113">Speichern Sie den Zertifikat Speicher unter Verwendung von [**certsavestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)in einem [*speicherblob*](../secgloss/b-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b971f-113">Save the certificate store to a memory [*BLOB*](../secgloss/b-gly.md) using [**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore).</span></span>
-   <span data-ttu-id="b971f-114">Bestimmen \# Sie mithilfe von [**cryptgetmessagesignercount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)die Anzahl der Signatur Geber der PKCS 7-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b971f-114">Determine the number of signers of the PKCS \#7 message using [**CryptGetMessageSignercount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount).</span></span>
-   <span data-ttu-id="b971f-115">Öffnen \# Sie mithilfe von [**cryptgetmessagecertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)einen Zertifikat Speicher aus einer PKCS 7-Nachricht im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b971f-115">Open a certificate store from a PKCS \#7 message in memory using [**CryptGetMessageCertificates**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates).</span></span>
-   <span data-ttu-id="b971f-116">Initialisieren des [**crypt- \_ Algorithmus- \_ Bezeichners**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) und der [**crypt- \_ Hash \_ Nachrichten \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_hash_message_para) -Struktur, die zum [*Hash*](../secgloss/h-gly.md) der Nachricht erforderlich</span><span class="sxs-lookup"><span data-stu-id="b971f-116">Initialize the [**CRYPT\_ALGORITHM\_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) and [**CRYPT\_HASH\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_hash_message_para) data structures needed to [*hash*](../secgloss/h-gly.md) the message</span></span>
-   <span data-ttu-id="b971f-117">Hash und Codieren der Nachricht mithilfe von [**crypthashmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage).</span><span class="sxs-lookup"><span data-stu-id="b971f-117">Hash and encode the message using [**CryptHashMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage).</span></span>
-   <span data-ttu-id="b971f-118">Stellen Sie fest, ob an einem geöffneten Zertifikat Speicher Änderungen vorgenommen wurden, und synchronisieren Sie den Speicher bei Bedarf mithilfe von " [**certcontrolstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)".</span><span class="sxs-lookup"><span data-stu-id="b971f-118">Determine whether changes have been made to an open certificate store and synchronizing the store if needed using [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore).</span></span>
-   <span data-ttu-id="b971f-119">Schließen eines Zertifikat Speicher mit " [**certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) " mit dem "CERT \_ Close \_ Store Force"- \_ \_ Flag.</span><span class="sxs-lookup"><span data-stu-id="b971f-119">Closing a certificate store using [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) with the CERT\_CLOSE\_STORE\_FORCE\_FLAG.</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example C program.
// This program demonstrates the use of the following functions:
//     CreateEvent
//     CertOpenStore
//     CertSetStoreProperty
//     CertGetStoreProperty
//     CryptFindLocalizedName 
//     CertSaveStore
//     CryptGetMessageSignerCount
//     CryptGetMessageCertificates
//     CryptHashMessage
//     CertControlStore
//     WaitForSingleObjectEx
//     CertCloseStore
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE hCertStore;     // Original certificate store
HCERTSTORE hNewStore;      // Store to be created 
                           // from a PKCS #7 message  
HANDLE     hEvent;
void *pvData;
DWORD cbData;
DWORD dwSignerCount;
CRYPT_DATA_BLOB Property_Name_Blob;   // BLOB to hold store property
CRYPT_DATA_BLOB Save_Store_Blob;      // BLOB to hold the PKCS #7 
                                      // message
CRYPT_HASH_MESSAGE_PARA      HashPara;  // Data structure used
                                        // to hash a message
const BYTE*                  rgpbToBeHashed[1];     
DWORD                        rgcbToBeHashed[1]; 
                                        // Arrays of messages to be
                                        // hashed
BYTE                         *pbHashedBlob;

DWORD                        cbHashedBlob;
                                        // Length of the hash BLOB
CRYPT_ALGORITHM_IDENTIFIER   AlgId;     // Data structure to hold the
                                        // hash algorithm identifier
BOOL                        fSignal;

//-------------------------------------------------------------------
// Initialize an event.

if(hEvent = CreateEvent(
    NULL,
    FALSE,          // Manual reset is FALSE.
    FALSE,          // The initial state of the event is FALSE.
    NULL))
{
     printf("An event has been created.\n");
}
else
{
     MyHandleError("The event was not created.");
}

//-------------------------------------------------------------------
// Open the MY certificate store. 

if ( hCertStore = CertOpenStore(
    CERT_STORE_PROV_SYSTEM,
    0,
    NULL,
    CERT_SYSTEM_STORE_CURRENT_USER,
    L"MY"))
{
     printf("The MY store is open.\n");
}
else
{
     MyHandleError("The MY store did not open.");
}

//-------------------------------------------------------------------
// Prepare a data structure to set a store property.
// Initialize the members of the CRYPT_DATA_BLOB.

Property_Name_Blob.pbData =(BYTE *) L"The Local MY Store";
Property_Name_Blob.cbData = 
       (wcslen((LPWSTR)Property_Name_Blob.pbData)+1) * sizeof(WCHAR);

//-------------------------------------------------------------------
// Set the store's localized name property.

if (CertSetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    0,
    &Property_Name_Blob))
{
     printf("The name of the store has been set. Continue. \n");
}
else
{
     MyHandleError("Setting the store's localized name failed.");
}
//-------------------------------------------------------------------
// Call CertGetStoreProperty a first time
// to get the length of the store name string to be returned.

if(CertGetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    NULL,     // NULL on the first call  
              // to establish the length of the string to
              // to be returned
    &cbData))
{
     printf("The length of the property is %d. \n",cbData);
}
else
{
     MyHandleError("The length of the property was not calculated.");
}

//-------------------------------------------------------------------
// cbData is the length of a string to be allocated. 
// Allocate the space for the string, and call the function a 
// the second time.

if(pvData = malloc(cbData))
{
  printf("%d bytes of memory allocated.\n",cbData);
}
else
{
     MyHandleError("Memory was not allocated.");
}
if(CertGetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    pvData,
    &cbData))
{
     printf("The localized name is %S.\n",pvData);
}
else
{
     MyHandleError("CertGetStoreProperty failed.");
}
//-------------------------------------------------------------------
//   Find and print the predefined localized name for the MY store.
//   Note that changing the localized store name property does not 
//   change the predefined localized store name.

printf("The predefined localized name of the MY "
       "store is still %S.\n", CryptFindLocalizedName(L"my"));

//-------------------------------------------------------------------
// Save the store to a PKCS #7 message in a file.

if(CertSaveStore(
   hCertStore,
   MY_ENCODING_TYPE,
   CERT_STORE_SAVE_AS_PKCS7,
   CERT_STORE_SAVE_TO_FILENAME_A,
   "pkcsseven.dat",
   0))
{
    printf("The store has been saved to a PKCS #7 message file.\n");
}
else
{
     MyHandleError("The store has not been saved.");
}

//-------------------------------------------------------------------
// Save the store to a PKCS #7 message in a file.
// Initialize the BLOB.

Save_Store_Blob.cbData=0;
Save_Store_Blob.pbData=NULL;

if(CertSaveStore(
   hCertStore,
   MY_ENCODING_TYPE,
   CERT_STORE_SAVE_AS_PKCS7,
   CERT_STORE_SAVE_TO_MEMORY,
   (void *)&Save_Store_Blob,
   0))
{
     printf("The store length, %d, has been determined.\n",
          Save_Store_Blob.cbData);
}
else
{
     MyHandleError("The store length could not be determined.");
}

if(Save_Store_Blob.pbData=(BYTE *) malloc(Save_Store_Blob.cbData))
{
     printf("Memory has been allocated.\n");
}
else
{
     MyHandleError("Memory allocation failure.");
}

if(CertSaveStore(
   hCertStore,
   MY_ENCODING_TYPE,
   CERT_STORE_SAVE_AS_PKCS7,
   CERT_STORE_SAVE_TO_MEMORY,
   (void *)&Save_Store_Blob,
   0))
{
     printf("The store has been saved to memory.\n");
}
else
{
     MyHandleError("The store was not saved to memory.");
}
//-------------------------------------------------------------------
//  Retrieve the number of signers of the PKCS #7 message.

if ( dwSignerCount = CryptGetMessageSignerCount(
     MY_ENCODING_TYPE,
     Save_Store_Blob.pbData,
     Save_Store_Blob.cbData))
{
     printf("The number of signers is %d.\n",dwSignerCount);
}
else
{
     printf("The number of signers is zero or could not"
         "be found.\n");
}
//-------------------------------------------------------------------
//   Open a certificate store from the PKCS #7 message stored to 
//   memory.

if(hNewStore=CryptGetMessageCertificates(
   MY_ENCODING_TYPE,
   NULL,
   0,
   Save_Store_Blob.pbData,
   Save_Store_Blob.cbData))
{
    printf("A new store has been opened from a PKCS #7.\n");
}
else
{
    MyHandleError("Opening the store from the PKCS #7 "
         "message failed.");
}
//-------------------------------------------------------------------
//  Next, hash the message.
//  Store the message and its length in the appropriate arrays.

rgpbToBeHashed[0]=Save_Store_Blob.pbData;
rgcbToBeHashed[0]=Save_Store_Blob.cbData;

//-------------------------------------------------------------------
//  Initialize the CRYPT_ALGORITHM_IDENTIFIER data structure.

AlgId.pszObjId=szOID_RSA_MD5;
AlgId.Parameters.cbData=0;

//-------------------------------------------------------------------
//  Initialize the CRYPT_HASH_MESSAGE_PARA data structure.

HashPara.cbSize = sizeof(CRYPT_HASH_MESSAGE_PARA);
HashPara.dwMsgEncodingType=MY_ENCODING_TYPE;
HashPara.hCryptProv=NULL;
HashPara.HashAlgorithm=AlgId;
HashPara.pvHashAuxInfo= NULL;

//-------------------------------------------------------------------
// Calculate the size of the hashed and encoded message. 

if(CryptHashMessage(
      &HashPara,
      FALSE,
      1,
      rgpbToBeHashed,
      rgcbToBeHashed,
      NULL,
      &cbHashedBlob,
      NULL,
      NULL))
{
     printf("The size of the hashed, encoded message is %d.\n",
          cbHashedBlob);
}
else
{
     MyHandleError("The size of the hash could not be determined.");
}

//-------------------------------------------------------------------
//  Allocated memory for the hashed, encoded BLOB.

if(pbHashedBlob = (BYTE*)malloc(cbHashedBlob))
{
     printf("Memory allocated for the hashed, encoded BLOB.\n");
}
else
{
     MyHandleError("Memory allocation failed.");
};

//-------------------------------------------------------------------
// Hash and encode the message.

if(CryptHashMessage(
       &HashPara,
       FALSE,
       1,
       rgpbToBeHashed,
       rgcbToBeHashed,
       pbHashedBlob,
       &cbHashedBlob,
       NULL,
       NULL))
{
     printf("The message has been hashed and encoded.\n");
}
else
{
     MyHandleError("The message was not hashed. ");
}

//-------------------------------------------------------------------
//  Call CertControlStore the first time with 
//  CERT_CONTROL_STORE_NOTIFY_CHANGE.

if(CertControlStore(
    hCertStore,                    // The store to be controlled
    0,                             // Not used 
    CERT_STORE_CTRL_NOTIFY_CHANGE, // Control action type
    &hEvent))                      // Points to the event handle.
                                   // When a change is detected,
                                   // a signal is written to the 
                                   // space pointed to by
                                   // hHandle.
{
  printf("Notify change worked \n");
}
else
{
  MyHandleError("Notify change failed. \n");
}
//-------------------------------------------------------------------
// Wait for the store to change.

fSignal =(WAIT_OBJECT_0 == WaitForSingleObjectEx(
    hEvent,
    1000 ,               // Number of milliseconds to wait.
                         // Use INFINITE to wait indefinitely for
                         // a change.
    FALSE));

if (fSignal)
//-------------------------------------------------------------------
// The store has changed.
// Call the function a second time with CERT_STORE_CTRL_RESYNC.
 
  if(CertControlStore(
          hCertStore,               // in, the store to be controlled
          0,                        // in, not used.
          CERT_STORE_CTRL_RESYNC,   // in, control action type
          &hEvent))                 // in, the handle of the event 
                                    // to be rearmed.
    printf("Resynchronization worked. \n");
  else
    MyHandleError("Resynchronization failed.");
else
{
  printf("The store was not changed. \n");
  printf("Resynchronization was not needed. \n");
}

// Free memory.

free (pbHashedBlob);

if(pvData)
     free(pvData);
if(CertCloseStore(
       hCertStore, 
       CERT_CLOSE_STORE_FORCE_FLAG))
{
     printf("The store has been closed. \n");
}
else
{
     MyHandleError("The store could not be closed.");
}
printf("The program ran to completion without error. \n");
}  // End main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to  
//  the standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
} // End of MyHandleError
```



 

 
