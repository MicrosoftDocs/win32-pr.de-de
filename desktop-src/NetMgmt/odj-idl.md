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
# <a name="offline-domain-join-idl-definitions"></a>IDL-Definitionen im Offline-Domänen Beitritt

## <a name="description"></a>BESCHREIBUNG

ODJ-Datenstrukturen (Offline-Domänen Beitritt) werden in einer C\C + +-Header Datei nicht definiert.  Stattdessen werden die Strukturen im IDL-Format (Interface Definition Language) definiert, das nach der Kompilierung für die Serialisierung und Deserialisierung verwendet wird. Auf der Windows-Plattform wird die Serialisierung und Deserialisierung dieser Strukturen automatisch durch die folgenden Win32-APIs behandelt:

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">"Nettrequestofflinedomainjoin"</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">Netkreateprovisioningpackage</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">"Nettrequestprovisioningpackagein Stall"</a>

In einigen Situationen, z. b. Interop mit nicht-Windows-Plattformen, ist es möglicherweise notwendig, eine manuelle Serialisierung und Deserialisierung durchzuführen. Dieses Thema enthält Definitionen für alle ODJ-Datenstrukturen in einer einzelnen IDL-Kompilierungseinheit und ist für die-Zusammenarbeit enthalten. Außerdem wird eine entsprechende Definition der Anwendungs Konfigurationsdatei (ACF) definiert. Dieser Inhalt wird nicht als Teil eines SDK bereitgestellt. Daher sollte der nachfolgende Inhalt in Ihren Code kopiert und mit einem IDL-Compiler kompiliert werden. Der IDL-Compiler erstellt die erforderlichen serialization\deserialization-Stub-Funktionen, die dann mit der Anwendung verknüpft werden. Weitere Informationen zur Serialisierung und Deserialisierung von Typen finden Sie unter <a href="/windows/win32/rpc/type-serialization">Typserialisierung</a> .

Ausführliche Informationen zur Element Dokumentation finden Sie in den Abschnitten zu den einzelnen Strukturen.

Wenn Sie den Microsoft-Mittell-Compiler verwenden, sollten Sie die folgenden Flags angeben, um die Kompatibilität zu maximieren:

/char unsigned

/ms_ext

/c_ext

## <a name="odj-idl-file"></a>ODJ-IDL-Datei

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

## <a name="odj-acf-file"></a>ODJ-ACF-Datei

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

## <a name="see-also"></a>Siehe auch

<a href="/windows/win32/midl/midl-start-page">Microsoft Interface Definition Language</a>

<a href="/windows/win32/midl/midl-command-line-reference">Mittlere Command-Line Referenz</a>

<a href="/windows/win32/rpc/serialization-services">Serialisierungsdienste</a>

<a href="/windows/win32/rpc/type-serialization">Typserialisierung</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">"Nettrequestofflinedomainjoin"</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">Netkreateprovisioningpackage</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">"Nettrequestprovisioningpackagein Stall"</a>
