---
title: IDL-Definitionen im Offline-Domänen Beitritt
description: IDL-Definitionen im Offline-Domänen Beitritt
ms.assetid: d495e2f0-5174-4d05-9297-4b4b0f200f08
ms.topic: article
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dec651c721cbe6bbf74123692137a01e528a82e5
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104391168"
---
# <a name="offline-domain-join-idl-definitions"></a><span data-ttu-id="e4a27-103">IDL-Definitionen im Offline-Domänen Beitritt</span><span class="sxs-lookup"><span data-stu-id="e4a27-103">Offline Domain Join IDL Definitions</span></span>

## <a name="description"></a><span data-ttu-id="e4a27-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4a27-104">Description</span></span>

<span data-ttu-id="e4a27-105">ODJ-Datenstrukturen (Offline-Domänen Beitritt) werden in einer C\C + +-Header Datei nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="e4a27-105">Offline Domain Join (ODJ) data structures are not defined in a C\C++ header file.</span></span>  <span data-ttu-id="e4a27-106">Stattdessen werden die Strukturen im IDL-Format (Interface Definition Language) definiert, das nach der Kompilierung für die Serialisierung und Deserialisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4a27-106">Instead, the structures are defined in Interface Definition Language (IDL) format which after compilation are used for serialization and deserialization.</span></span> <span data-ttu-id="e4a27-107">Auf der Windows-Plattform wird die Serialisierung und Deserialisierung dieser Strukturen automatisch durch die folgenden Win32-APIs behandelt:</span><span class="sxs-lookup"><span data-stu-id="e4a27-107">On the Windows platform serialization and deserialization of these structures is handled automatically by the following Win32 APIs:</span></span>

<span data-ttu-id="e4a27-108"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-108"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span></span>

<span data-ttu-id="e4a27-109"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">"Nettrequestofflinedomainjoin"</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-109"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a></span></span>

<span data-ttu-id="e4a27-110"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">Netkreateprovisioningpackage</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-110"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a></span></span>

<span data-ttu-id="e4a27-111"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">"Nettrequestprovisioningpackagein Stall"</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-111"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a></span></span>

<span data-ttu-id="e4a27-112">In einigen Situationen, z. b. Interop mit nicht-Windows-Plattformen, ist es möglicherweise notwendig, eine manuelle Serialisierung und Deserialisierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="e4a27-112">In some situations, for example interop with non-Windows platforms, it may be necessary to do manual serialization and deserialization.</span></span> <span data-ttu-id="e4a27-113">Dieses Thema enthält Definitionen für alle ODJ-Datenstrukturen in einer einzelnen IDL-Kompilierungseinheit und ist für die-Zusammenarbeit enthalten.</span><span class="sxs-lookup"><span data-stu-id="e4a27-113">This topic contains definitions for all of the ODJ data structures in a single IDL compilation unit and is included for convienence.</span></span> <span data-ttu-id="e4a27-114">Außerdem wird eine entsprechende Definition der Anwendungs Konfigurationsdatei (ACF) definiert.</span><span class="sxs-lookup"><span data-stu-id="e4a27-114">A matching Application Configuration File (ACF) definition is also defined.</span></span> <span data-ttu-id="e4a27-115">Dieser Inhalt wird nicht als Teil eines SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e4a27-115">This content is not provided as part of any SDK.</span></span> <span data-ttu-id="e4a27-116">Daher sollte der nachfolgende Inhalt in Ihren Code kopiert und mit einem IDL-Compiler kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="e4a27-116">Therefore the content below should be copied into your code and compiled with an IDL compiler.</span></span> <span data-ttu-id="e4a27-117">Der IDL-Compiler erstellt die erforderlichen serialization\deserialization-Stub-Funktionen, die dann mit der Anwendung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="e4a27-117">The IDL compiler will produce the necessary serialization\deserialization stub functions, which are then linked into your application.</span></span> <span data-ttu-id="e4a27-118">Weitere Informationen zur Serialisierung und Deserialisierung von Typen finden Sie unter <a href="/windows/win32/rpc/type-serialization">Typserialisierung</a> .</span><span class="sxs-lookup"><span data-stu-id="e4a27-118">See <a href="/windows/win32/rpc/type-serialization">Type Serialization</a> for more details on how type serialization and deserialization.</span></span>

<span data-ttu-id="e4a27-119">Ausführliche Informationen zur Element Dokumentation finden Sie in den Abschnitten zu den einzelnen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e4a27-119">Refer to the individual structure sections for detailed member documentation.</span></span>

<span data-ttu-id="e4a27-120">Wenn Sie den Microsoft-Mittell-Compiler verwenden, sollten Sie die folgenden Flags angeben, um die Kompatibilität zu maximieren:</span><span class="sxs-lookup"><span data-stu-id="e4a27-120">If you are using the Microsoft MIDL compiler, you should specify the following flags to maximize compatibility:</span></span>

<span data-ttu-id="e4a27-121">/char unsigned</span><span class="sxs-lookup"><span data-stu-id="e4a27-121">/char unsigned</span></span>

<span data-ttu-id="e4a27-122">/ms_ext</span><span class="sxs-lookup"><span data-stu-id="e4a27-122">/ms_ext</span></span>

<span data-ttu-id="e4a27-123">/c_ext</span><span class="sxs-lookup"><span data-stu-id="e4a27-123">/c_ext</span></span>

## <a name="odj-idl-file"></a><span data-ttu-id="e4a27-124">ODJ-IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="e4a27-124">ODJ IDL File</span></span>

```C++
include "dsgetdc.h";

interface ODJ
{
    typedef struct _ODJ_BLOB
    {
        ULONG ulODJFormat;
        ULONG cbBlob;
        [size_is(cbBlob)] PBYTE pBlob;
    } ODJ_BLOB, *PODJ_BLOB;

    typedef struct _ODJ_PROVISION_DATA
    {
        ULONG ulVersion;
        ULONG ulcBlobs;
        [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
    } ODJ_PROVISION_DATA;

    typedef ODJ_PROVISION_DATA *PODJ_PROVISION_DATA;

    typedef struct _OP_BLOB
    {
        ULONG                       cbBlob;
        [size_is(cbBlob)]   PBYTE   pBlob;

    } OP_BLOB, *POP_BLOB;

    typedef struct _OP_PACKAGE_PART
    {
        GUID    PartType;
        ULONG   ulFlags;
        OP_BLOB Part;
        OP_BLOB Extension;
    } OP_PACKAGE_PART, *POP_PACKAGE_PART;

    typedef struct _OP_PACKAGE_PART_COLLECTION
    {
        ULONG                                 cParts;
        [size_is(cParts)]   POP_PACKAGE_PART  pParts;
        OP_BLOB                               Extension;
    } OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;

    typedef struct _OP_PACKAGE
    {
        GUID    EncryptionType;
        OP_BLOB EncryptionContext;
        OP_BLOB WrappedPartCollection;
        ULONG   cbDecryptedPartCollection;
        OP_BLOB Extension;
    } OP_PACKAGE, *POP_PACKAGE;

    typedef struct _SID_IDENTIFIER_AUTHORITY
    {
        UCHAR Value[6];
    } SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;

    typedef struct _ODJ_SID
    {
        UCHAR Revision;
        UCHAR SubAuthorityCount;
        SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
        [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
    }   ODJ_SID, *PODJ_SID;

    typedef struct _ODJ_UNICODE_STRING
    {
        USHORT Length;
        USHORT MaximumLength;
        [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
    } ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;

    typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
    {
        ODJ_UNICODE_STRING Name;
        ODJ_UNICODE_STRING DnsDomainName;
        ODJ_UNICODE_STRING DnsForestName;
        GUID DomainGuid;
        PODJ_SID Sid;
    }   ODJ_POLICY_DNS_DOMAIN_INFO;

    typedef struct _ODJ_WIN7BLOB
    {
        [string] wchar_t *lpDomain;
        [string] wchar_t *lpMachineName;
        [string] wchar_t *lpMachinePassword;
        ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
        DOMAIN_CONTROLLER_INFOW DcInfo;
        DWORD Options;
    } ODJ_WIN7BLOB;

    typedef ODJ_WIN7BLOB *PODJ_WIN7BLOB;

    cpp_quote("#define OP_JP2_FLAG_PERSISTENTSITE    0x00000001")

    typedef struct _OP_JOINPROV2_PART
    {
        DWORD     dwFlags;
        [string] wchar_t *lpNetbiosName;
        [string] wchar_t *lpSiteName;
        [string] wchar_t *lpPrimaryDNSDomain;

        DWORD             dwReserved;
        [string] wchar_t *lpReserved;
    } OP_JOINPROV2_PART, *POP_JOINPROV2_PART;

    typedef struct _OP_JOINPROV3_PART
    {
        DWORD Rid;
        [string] wchar_t *lpSid;
    } OP_JOINPROV3_PART, *POP_JOINPROV3_PART;

    typedef struct _OP_POLICY_ELEMENT
    {
        [string] wchar_t                *pKeyPath;
        [string] wchar_t                *pValueName;
        ULONG                           ulValueType;
        ULONG                           cbValueData;
        [size_is(cbValueData)]  PBYTE   pValueData;
    } OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;

    typedef struct _OP_POLICY_ELEMENT_LIST
    {
        [string] wchar_t                            *pSource;
        ULONG                                       ulRootKeyId;
        ULONG                                       cElements;
        [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
    } OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;

    typedef struct _OP_POLICY_PART
    {
        ULONG                                       cElementLists;
        [size_is(cElementLists)]
                            POP_POLICY_ELEMENT_LIST pElementLists;
        OP_BLOB                                     Extension;
    } OP_POLICY_PART, *POP_POLICY_PART;

    typedef struct _OP_CERT_PFX_STORE
    {
        [string] wchar_t            *pTemplateName;
        ULONG                       ulPrivateKeyExportPolicy;
        [string] wchar_t            *pPolicyServerUrl;
        ULONG                       ulPolicyServerUrlFlags;
        [string] wchar_t            *pPolicyServerId;
        ULONG                       cbPfx;
        [size_is(cbPfx)]    PBYTE   pPfx;
    } OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;

    typedef struct _OP_CERT_SST_STORE
    {
        ULONG                       StoreLocation;
        [string] wchar_t            *pStoreName;
        ULONG                       cbSst;
        [size_is(cbSst)]    PBYTE   pSst;
    } OP_CERT_SST_STORE, *POP_CERT_SST_STORE;

    typedef struct _OP_CERT_PART
    {
        ULONG                                       cPfxStores;
        [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
        ULONG                                       cSstStores;
        [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
        OP_BLOB                                     Extension;
    } OP_CERT_PART, *POP_CERT_PART;
}
```

## <a name="odj-acf-file"></a><span data-ttu-id="e4a27-125">ODJ-ACF-Datei</span><span class="sxs-lookup"><span data-stu-id="e4a27-125">ODJ ACF File</span></span>

```C++
[
    // If necessary for your application, see MIDL documentation for alternatives to explicit_handle
    explicit_handle
]
interface ODJ
{
    typedef [encode, decode] PODJ_WIN7BLOB;
    typedef [encode, decode] POP_JOINPROV2_PART;
    typedef [encode, decode] POP_JOINPROV3_PART;
    typedef [encode, decode] PODJ_PROVISION_DATA;
    typedef [encode, decode] POP_PACKAGE_PART;
    typedef [encode, decode] POP_PACKAGE_PART_COLLECTION;
    typedef [encode, decode] POP_PACKAGE;
    typedef [encode, decode] POP_POLICY_PART;
    typedef [encode, decode] POP_CERT_PART;
}
```

## <a name="see-also"></a><span data-ttu-id="e4a27-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4a27-126">See also</span></span>

<span data-ttu-id="e4a27-127"><a href="/windows/win32/midl/midl-start-page">Microsoft Interface Definition Language</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-127"><a href="/windows/win32/midl/midl-start-page">Microsoft Interface Definition Language</a></span></span>

<span data-ttu-id="e4a27-128"><a href="/windows/win32/midl/midl-command-line-reference">Mittlere Command-Line Referenz</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-128"><a href="/windows/win32/midl/midl-command-line-reference">MIDL Command-Line Reference</a></span></span>

<span data-ttu-id="e4a27-129"><a href="/windows/win32/rpc/serialization-services">Serialisierungsdienste</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-129"><a href="/windows/win32/rpc/serialization-services">Serialization Services</a></span></span>

<span data-ttu-id="e4a27-130"><a href="/windows/win32/rpc/type-serialization">Typserialisierung</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-130"><a href="/windows/win32/rpc/type-serialization">Type Serialization</a></span></span>

<span data-ttu-id="e4a27-131"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-131"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span></span>

<span data-ttu-id="e4a27-132"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">"Nettrequestofflinedomainjoin"</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-132"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a></span></span>

<span data-ttu-id="e4a27-133"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">Netkreateprovisioningpackage</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-133"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a></span></span>

<span data-ttu-id="e4a27-134"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">"Nettrequestprovisioningpackagein Stall"</a></span><span class="sxs-lookup"><span data-stu-id="e4a27-134"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a></span></span>
