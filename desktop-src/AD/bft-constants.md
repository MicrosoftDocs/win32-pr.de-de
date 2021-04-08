---
title: Bft-Konstanten (ntdsbcli. h)
description: Die bft-Konstanten werden als Bitflags verwendet, um unterschiedliche Dateitypen in einer Active Directory Domain Services Sicherung zu identifizieren.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949722"
---
# <a name="bft-constants"></a>Bft-Konstanten

Die bft-Konstanten werden als Bitflags verwendet, um unterschiedliche Dateitypen in einer Active Directory Domain Services Sicherung zu identifizieren.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**bft- \_ Protokoll \_ Verzeichnis**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



Die Datei gehört zum Protokoll Verzeichnis.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**bft- \_ Daten Bank \_ Verzeichnis**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



Die Datei gehört zum Datenbankverzeichnis.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**bft- \_ Verzeichnis**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Der angegebene Pfad ist ein Verzeichnis und kein Dateiname.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**bft- \_ Protokoll**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Gibt eine Protokolldatei an, die zum Protokoll Verzeichnis gehört.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**bft- \_ Protokoll Verzeichnis \_**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



Die Datei ist der Pfad des Protokoll Verzeichnisses.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**bft-Prüf Punkt Verzeichnis \_ \_**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



Die Datei ist der Pfad des Checkpoint-Verzeichnisses.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**bft- \_ NTDS- \_ Datenbank**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



Bei der Datei handelt es sich um eine Verzeichnisdienst-Datenbank, die im Datenbankverzeichnis gehört.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**bft \_ - \_ Patchdatei**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



Bei der Datei handelt es sich um eine Patchdatei, die zum Protokoll Verzeichnis gehört.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**bft \_ unbekannt**
</dt> <dd> <dl> <dt>

0x0f
</dt> <dt>



Die Datei kann nicht erkannt werden. Die Datei stimmt nicht mit den bekannten Dateinamen und Dateitypen überein.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |



 

 





