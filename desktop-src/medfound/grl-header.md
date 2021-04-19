---
description: Enthält den GRL-Header (Global Sperrlist).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: GRL_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342785"
---
# <a name="grl_header-structure"></a>GRL- \_ Header Struktur

Enthält den GRL-Header (Global Sperrlist).

## <a name="syntax"></a>Syntax


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**wszidentifier**
</dt> <dd>

Der GRL-Bezeichner. Der Wert ist immer L "msgrl".

</dd> <dt>

**wformatmajor**
</dt> <dd>

Die Hauptversionsnummer. Der Wert muss derzeit 1 lauten.

</dd> <dt>

**wformatminor**
</dt> <dd>

Die Nebenversionsnummer. Derzeit muss der Wert 0 (null) sein.

</dd> <dt>

**CreationTime**
</dt> <dd>

Ein **FILETIME** -Wert, der angibt, wann die Datei erstellt wurde.

</dd> <dt>

**dwsequencenumschlag**
</dt> <dd>

Die GRL-Versionsnummer. Der Wert muss aktuell mindestens 3 sein.

</dd> <dt>

**dwforcerebootversion**
</dt> <dd>

Reserviert.

</dd> <dt>

**dwforceprocessrestartversion**
</dt> <dd>

Reserviert.

</dd> <dt>

**cbrevocationsectionoffset**
</dt> <dd>

Der Offset in Bytes vom Anfang der GRL zum Core-Abschnitt.

</dd> <dt>

**"krevokedkernelbinaries"**
</dt> <dd>

Die Anzahl der in der GRL aufgelisteten, gesperrten Kernel-Binärdateien.

</dd> <dt>

**"krevokeduserbinaries"**
</dt> <dd>

Die Anzahl der gesperrten Binärdateien im Benutzermodus, die in der GRL aufgeführt sind.

</dd> <dt>

**"krevokedzertifikate"**
</dt> <dd>

Die Anzahl der in der GRL aufgeführten gesperrten Zertifikate.

</dd> <dt>

**ctreudroots**
</dt> <dd>

Die Anzahl der in der GRL aufgelisteten vertrauenswürdigen Stämme.

</dd> <dt>

**cbextensiblesectionoffset**
</dt> <dd>

Der Offset in Bytes vom Anfang der GRL bis zum Extensible-Abschnitt.

</dd> <dt>

**cextensibleentries**
</dt> <dd>

Die Anzahl der Einträge im Extensible-Abschnitt.

</dd> <dt>

**cbrenewalsectionoffset**
</dt> <dd>

Der Offset in Bytes vom Anfang der GRL bis zum Verlängerungen-Abschnitt.

</dd> <dt>

**"krevokedkernelbinaryverlängerungen"**
</dt> <dd>

Die Anzahl der binären Kernel-Erneuerungen, die in der GRL aufgeführt sind.

</dd> <dt>

**"krevokeduserbinaryerneuerals"**
</dt> <dd>

Die Anzahl der Binär Erneuerungen im Benutzermodus, die in der GRL aufgeführt sind.

</dd> <dt>

**"krevokedcertificaterenewals"**
</dt> <dd>

Die Anzahl der Zertifikat Erneuerungen, die in der GRL aufgeführt sind.

</dd> <dt>

**cbsignaturecoreoffset**
</dt> <dd>

Der Offset in Bytes vom Anfang der GRL bis zur Kern Abschnitts Signatur.

</dd> <dt>

**cbsignatureexum ffset**
</dt> <dd>

Der Offset in Bytes vom Anfang der GRL bis zur erweiterbaren Abschnitts Signatur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle ganzzahligen Werte in der GRL haben eine Little-Endian-Byte Reihe. Alle-Strukturen sind auf 1-Byte-Grenzen ausgerichtet.

Diese Struktur ist nicht in einem SDK-Header deklariert. Um diese Struktur zu verwenden, fügen Sie die hier gezeigte Deklaration dem Quellcode hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Zertifikat Sperrung](opm-certificate-revocation.md)
</dt> <dt>

[OPM-Strukturen](opm-structures.md)
</dt> </dl>

 

 




