---
description: Im folgenden Beispiel wird das Konzept des Sammlungs Speichers veranschaulicht. dabei handelt es sich um einen temporären Zertifikat Speicher, in dem der Inhalt mehrerer Zertifikat Speicher enthalten ist.
ms.assetid: 5349222f-ad68-477c-8712-fde16e68f600
title: 'Beispiel-C-Programm: Sammlungs-und gleich geordnete Zertifikat Speichervorgänge'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ad1957f37e1aabeabbda0be8c14662c14c3ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960260"
---
# <a name="example-c-program-collection-and-sibling-certificate-store-operations"></a><span data-ttu-id="144c7-103">Beispiel-C-Programm: Sammlungs-und gleich geordnete Zertifikat Speichervorgänge</span><span class="sxs-lookup"><span data-stu-id="144c7-103">Example C Program: Collection and Sibling Certificate Store Operations</span></span>

<span data-ttu-id="144c7-104">Im folgenden Beispiel wird das Konzept des Sammlungs Speichers veranschaulicht. dabei handelt es sich um einen temporären [*Zertifikat Speicher*](../secgloss/c-gly.md) , in dem der Inhalt mehrerer Zertifikat Speicher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="144c7-104">The following example demonstrates the concept of the collection store, a temporary [*certificate store*](../secgloss/c-gly.md) that actually includes the contents of several certificate stores.</span></span> <span data-ttu-id="144c7-105">Ein oder mehrere Speicher können einer Auflistung hinzugefügt werden, die mit einem einzelnen Funktions aufrufauf den Inhalt aller Geschäfte in der Sammlung zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="144c7-105">One or more stores may be added to a collection that can access the contents of any of the stores in the collection with a single function call.</span></span>

<span data-ttu-id="144c7-106">In diesem Beispiel werden die folgenden Aufgaben und [*kryptoapi*](../secgloss/c-gly.md) -Funktionen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="144c7-106">This example illustrates the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="144c7-107">Öffnen und Schließen eines Sammlungs Speichers, eines Speicher Speichers und eines System Speichers mit " [**certopsstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) " und " [**certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)".</span><span class="sxs-lookup"><span data-stu-id="144c7-107">Opening and closing a collection store, a memory store and a system store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) and [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span></span>
-   <span data-ttu-id="144c7-108">Hinzufügen eines gleich geordneten Stores zu einem Sammlungs Speicher mithilfe von [**certaddstoreeincollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span><span class="sxs-lookup"><span data-stu-id="144c7-108">Adding a sibling store to a collection store using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span>
-   <span data-ttu-id="144c7-109">Suchen von Zertifikaten und Links zu Zertifikaten in Stores, die einige Kriterien mithilfe von " [**certfindcertifikateinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)" erfüllen.</span><span class="sxs-lookup"><span data-stu-id="144c7-109">Finding certificates and links to certificates in stores that meets some criteria using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="144c7-110">Hinzufügen eines abgerufenen Zertifikats zu einem Speicher im Arbeitsspeicher mithilfe von [**certaddcertifikatecontexttostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore).</span><span class="sxs-lookup"><span data-stu-id="144c7-110">Adding a retrieved certificate to a store in memory using [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore).</span></span>
-   <span data-ttu-id="144c7-111">Hinzufügen eines Links zu einem Zertifikat zu einem Speicher mithilfe von [**certaddcertifikatelinktostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore).</span><span class="sxs-lookup"><span data-stu-id="144c7-111">Adding a link to a certificate to a store using [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore).</span></span>
-   <span data-ttu-id="144c7-112">Speichern des Speichers im Arbeitsspeicher in einer Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="144c7-112">Saving the store in memory to a file on disk.</span></span>
-   <span data-ttu-id="144c7-113">Öffnen und Schließen eines dateibasierten Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="144c7-113">Opening and closing a file-based certificate store.</span></span>
-   <span data-ttu-id="144c7-114">Entfernen eines gleich geordneten Speicher Orts aus einer Sammlung mithilfe von [**certrerovestorefromcollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).</span><span class="sxs-lookup"><span data-stu-id="144c7-114">Removing a sibling store from a collection using [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).</span></span>

<span data-ttu-id="144c7-115">In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="144c7-115">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="144c7-116">Der Code für diese Funktion ist im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="144c7-116">The code for this function is included with the sample.</span></span> <span data-ttu-id="144c7-117">Der Code für dieses und andere Hilfsfunktionen ist auch unter [universell Funktionen](general-purpose-functions.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="144c7-117">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>

<span data-ttu-id="144c7-118">In diesem Beispiel wird die im Thema [Erstellen einer DACL](../secbp/creating-a-dacl.md) definierte Funktion "-Funktion" verwendet, um sicherzustellen, **dass die geöffnete** Datei mit einer ordnungsgemäßen DACL erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="144c7-118">This example uses the **CreateMyDACL** function, defined in the [Creating a DACL](../secbp/creating-a-dacl.md) topic, to ensure the open file is created with a proper DACL.</span></span>

<span data-ttu-id="144c7-119">Im folgenden Beispiel wird ein Sammlungs Speicher geöffnet, ein neuer Zertifikat Speicher im Arbeitsspeicher erstellt, und der neue Speicher wird dem Sammlungs Speicher als gleich geordneter Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="144c7-119">The following example opens a collection store, creates a new certificate store in memory, and adds the new store as a sibling store to the collection store.</span></span> <span data-ttu-id="144c7-120">Das Programm öffnet dann einen Systemspeicher und ruft ein Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="144c7-120">The program then opens a system store and retrieves a certificate.</span></span> <span data-ttu-id="144c7-121">Dieses Zertifikat wird dem Speicher Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="144c7-121">That certificate is added to the memory store.</span></span> <span data-ttu-id="144c7-122">Ein zweites Zertifikat wird aus dem Systemspeicher abgerufen, und es wird ein Link zu diesem Zertifikat zum Speicher Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="144c7-122">A second certificate is retrieved from the system store and a link to that certificate is added to the memory store.</span></span> <span data-ttu-id="144c7-123">Das Zertifikat und der Link werden dann aus dem Sammlungs Speicher abgerufen, und es wird angezeigt, dass Zertifikate und Verknüpfungen in einem gleich geordneten Speicher aus dem Sammlungs Speicher abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="144c7-123">The certificate and the link are then retrieved from the collection store showing that certificates and links in a sibling store can be retrieved from the collection store.</span></span> <span data-ttu-id="144c7-124">Der Arbeitsspeicher wird auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="144c7-124">The memory is saved to disk.</span></span> <span data-ttu-id="144c7-125">Der Speicher Speicher wird dann aus der Sammlung entfernt.</span><span class="sxs-lookup"><span data-stu-id="144c7-125">The memory store is then removed from the collection.</span></span> <span data-ttu-id="144c7-126">Der dem Speicher Speicher hinzugefügte Link befindet sich weiterhin im Speicher Speicher, kann aber nicht mehr im Sammlungs Speicher gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="144c7-126">The link added to the memory store can still be found in the memory store but can no longer be found in the collection store.</span></span> <span data-ttu-id="144c7-127">Alle Filialen und Dateien werden geschlossen, und der Dateispeicher wird erneut geöffnet, und für den Zertifikat Link wird eine Suche durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="144c7-127">All of the stores and files are closed, then the file store is reopened and a search is done for the certificate link.</span></span> <span data-ttu-id="144c7-128">Der Erfolg dieses Programms hängt von der Verfügbarkeit meines Stores ab.</span><span class="sxs-lookup"><span data-stu-id="144c7-128">The success of this program depends upon a My store being available.</span></span> <span data-ttu-id="144c7-129">Dieser Speicher muss ein Zertifikat mit dem Betreff "INSERT \_ CERT \_ Subject \_ Name1" und ein zweites Zertifikat mit dem Betreff "CERT- \_ \_ Betreff \_ name2 einfügen" enthalten.</span><span class="sxs-lookup"><span data-stu-id="144c7-129">That store must include a certificate with the subject "Insert\_cert\_subject\_name1" and a second certificate with the subject "Insert\_cert\_subject\_name2".</span></span> <span data-ttu-id="144c7-130">Die Namen der Antragsteller müssen in die Namen von Zertifikat Subjekten geändert werden, die bekanntermaßen im My-Speicher sind.</span><span class="sxs-lookup"><span data-stu-id="144c7-130">The names of the subjects should be changed to the names of certificate subjects known to be in the My store.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define  MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HCERTSTORE  hCollectionStore;           // Collection store 
                                        // handle
HCERTSTORE  hSystemStore;               // System store handle
HCERTSTORE  hMemoryStore;               // Memory store handle
PCCERT_CONTEXT  pDesiredCert = NULL;    // Set to NULL for the first 
                                        // call to
                                        // CertFindCertificateInStore
HANDLE hStoreFileHandle ;               // Output file handle
LPWSTR pszFileName = L"TestStor.sto";    // Output file name
SECURITY_ATTRIBUTES sa;                 // for DACL
LPWSTR pswzFirstCert = L"Insert_cert_subject_name1";
                                        // Subject of the first 
                                        // certificate
LPWSTR pswzSecondCert = L"Insert_cert_subject_name2";    
                                        // Subject of the second
                                        // certificate

//-------------------------------------------------------------------
// Open a collection certificate store.

if(hCollectionStore = CertOpenStore(
      CERT_STORE_PROV_COLLECTION, // Collection store
      0,                          // Encoding type 
                                  // Not used with a collection store
      NULL,                       // Use the default provider
      0,                          // No flags
      NULL))                      // Not needed
{
   printf("Opened a collection store. \n");
}
else
{
   MyHandleError( "Error opening the collection store.");
}
//-------------------------------------------------------------------
// Open a new certificate store in memory.

if(hMemoryStore = CertOpenStore(
      CERT_STORE_PROV_MEMORY,    // Memory store
      0,                         // Encoding type
                                 // not used with a memory store
      NULL,                      // Use the default provider
      0,                         // No flags
      NULL))                     // Not needed
{
   printf("Opened a memory store. \n");
}
else
{
   MyHandleError( "Error opening a memory store.");
}
//-------------------------------------------------------------------
// Open the My system store using CertOpenStore.

if(hSystemStore = CertOpenStore(
     CERT_STORE_PROV_SYSTEM, // System store will be a 
                             // virtual store
     0,                      // Encoding type not needed 
                             // with this PROV
     NULL,                   // Accept the default HCRYPTPROV
     CERT_SYSTEM_STORE_CURRENT_USER,
     L"MY"))                 // System store name
{
   printf("Opened the My system store. \n");
}
else
{
   MyHandleError( "Could not open the My system store.");
}
//-------------------------------------------------------------------
// Get a certificate that has the string
// "Insert_cert_subject_name1" in its subject. 
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzFirstCert,               // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found. \n",pswzFirstCert);
}
else
{
   MyHandleError("Could not find the desired certificate.");
}
//-------------------------------------------------------------------
// pDesiredCert is a pointer to a certificate with a subject that 
// includes the string passed as parameter five to the function.

//-------------------------------------------------------------------
// Add the certificate from the My store to the memory store.

if(CertAddCertificateContextToStore(
      hMemoryStore,                // Store handle
      pDesiredCert,                // Pointer to a certificate
      CERT_STORE_ADD_USE_EXISTING,
      NULL))
{
   printf("Certificate added to the memory store. \n");
}
else
{
   MyHandleError("Could not add the certificate to the "
       "memory store.");
}

//-------------------------------------------------------------------
//  Add the memory store as a sibling to the collection store. 
//  All certificates in the memory store will now be available in
//  the collection store. Any new certificates added to the memory 
//  store will also be available in the collection store.

if(CertAddStoreToCollection(
   hCollectionStore,
   hMemoryStore,
   CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG,// New certificates can be
                                       // added to the sibling store
   1))                                 // The sibling store's 
                                       // priority
                                       // because this store has 
                                       // the highest priority, 
                                       // certificates added to
                                       // the collection store will
                                       // actually be stored in this
                                       // store
{
     printf("The memory store is added to the collection store.\n");
}
else
{
     MyHandleError("The memory store was not added "
         "to the collection.");
}
//-------------------------------------------------------------------
//  Find a different certificate in the My store, and add, to the 
//  memory store, a link to that certificate.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzSecondCert,              // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found. \n",pswzSecondCert);
}
else
{
   MyHandleError("Could not find the second certificate.");
}
//-------------------------------------------------------------------
// Add a link to a second certificate from the My store to the new 
// memory store.

if(CertAddCertificateLinkToStore(
      hMemoryStore,                // store handle
      pDesiredCert,                // pointer to a certificate
      CERT_STORE_ADD_USE_EXISTING,
      NULL))
{
   printf("%S link added to the memory store. \n",pswzSecondCert);
}
else
{
   MyHandleError("Could not add the certificate link to the "
       "memory store.");
}

//-------------------------------------------------------------------
// Find the first certificate in the memory store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,                // Store handle
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzFirstCert,               // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found in the "
      "memory store. \n",pswzFirstCert);
}
else
{
   printf("The %S certificate was not in the "
       "memory store.\n", pswzFirstCert);
}

//-------------------------------------------------------------------
//  Find that same certificate in the collection store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hCollectionStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzFirstCert,               // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S certificate was found in the "
      "collection store. \n", pswzFirstCert);
}
else
{
  printf("The %S certificate was not in the "
      "memory collection.\n", pswzFirstCert);
}

//-------------------------------------------------------------------
//  Find the certificate link in the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hCollectionStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // Mo dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzSecondCert,              // The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S link was found in the "
      "collection store. \n", pswzSecondCert);
}
else
{
   printf("The %S certificate link was not in the "
       "memory store.\n", pswzSecondCert);
}

//-------------------------------------------------------------------
// Create a file to save the new store and certificate into.

// Create a DACL for the file.
sa.nLength = sizeof(SECURITY_ATTRIBUTES);
sa.bInheritHandle = FALSE;  

// Call function to set the DACL. The DACL
// is set in the SECURITY_ATTRIBUTES 
// lpSecurityDescriptor member.
// if CreateMyDACL(&sa) fails, call MyHandleError("CreateMyDACL failed.")

if(hStoreFileHandle = CreateFile(
      pszFileName,             // File path
      GENERIC_WRITE,           // Access mode
      0,                       // Share mode
      &sa,                     // Security 
      CREATE_ALWAYS,           // How to create the file
      FILE_ATTRIBUTE_NORMAL,   // File attributes
      NULL))                   // File template
{
   printf("Created a new file on disk. \n");
}
else
{
   MyHandleError("Could not create a file on disk.");
}
//-------------------------------------------------------------------
// hStoreFileHandle is the output file handle.
// Save the memory store and its certificate to the output file.

if( CertSaveStore(
      hMemoryStore,            // Store handle
      0,                       // Encoding type not needed here
      CERT_STORE_SAVE_AS_STORE,
      CERT_STORE_SAVE_TO_FILE,
      hStoreFileHandle,        // The handle of an open disk file
      0))                      // dwFlags--no flags are needed here
{
   printf("Saved the memory store to disk. \n");
}
else
{
   MyHandleError("Could not save the memory store to disk.");
}
//-------------------------------------------------------------------
//  Remove the sibling store from the collection.
//  CertRemoveStoreFromCollection returns void.

printf("\nRemoving the memory store from the collection.\n");
CertRemoveStoreFromCollection(
    hCollectionStore,
    hMemoryStore);

//-------------------------------------------------------------------
//   Find the link in the memory store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      pswzSecondCert,              // Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL is used so that the 
                                   // search will begin at the 
                                   // beginning of the certificate
                                   // store
{
  printf("The %S link is still in the "
      "memory store. \n", pswzSecondCert);
}
else
{
   printf("The certificate link was not in the "
       "memory store.\n");
}
//-------------------------------------------------------------------
//  Try to find certificate link in the collection store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hCollectionStore,
      MY_ENCODING_TYPE,            
      0, 
      CERT_FIND_SUBJECT_STR,    
      pswzSecondCert,
      NULL))       
{
  printf("The %S link was found in the "
      "collection store. \n", pswzSecondCert);
}
else
{
   printf("Removing the store from the collection worked.\n");
   printf("The %S link is not in the "
       "collection store.\n",pswzSecondCert);
}
//-------------------------------------------------------------------
// Close the stores and the file. Reopen the file store, 
// and check its contents.

if(hMemoryStore)
    CertCloseStore(
        hMemoryStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

if(hSystemStore)
    CertCloseStore(
        hSystemStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

if(hStoreFileHandle)
     CloseHandle(hStoreFileHandle);

printf("All of the stores and files are closed. \n");

//-------------------------------------------------------------------
//  Reopen the file store.

if(hMemoryStore = CertOpenStore(
       CERT_STORE_PROV_FILENAME,    // Store provider type
       MY_ENCODING_TYPE,            // If needed, use the usual
                                    // encoding types
       NULL,                        // Use the default HCRYPTPROV
       0,                           // Accept the default for all
                                    // dwFlags
       L"TestStor.sto" ))           // The name of an existing file
                                    // as a Unicode string
{
     printf("The file store has been reopened. \n");
}
else
{
    printf("The file store could not be reopened. \n");
}
//-------------------------------------------------------------------
//  Find the certificate link in the reopened file store.
if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            
      0,                          
      CERT_FIND_SUBJECT_STR,      
      pswzSecondCert,              
      NULL))                       
{
  printf("The %S certificate link was found in the "
      "file store. \n",pswzSecondCert);
}
else
{
   printf("The certificate link was not in the file store.\n");
}

//-------------------------------------------------------------------
// Clean up memory and end.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(hMemoryStore)
    CertCloseStore(
        hMemoryStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

printf("All of the stores and files are closed. \n");

} // End of main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function, to print an error message to the standard error 
// (stderr) file and exit the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 
