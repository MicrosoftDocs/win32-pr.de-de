---
title: BFT-Konstanten (Ntdsbcli.h)
description: Die BFT-Konstanten werden als Bitflags verwendet, um verschiedene Dateitypen in einer Active Directory Domain Services identifizieren.
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
ms.openlocfilehash: 3b5e9275e01b8c33d308b55b2638d4eaf186b8f5265834acc27acd2f146f0d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024049"
---
# <a name="bft-constants"></a>BFT-Konstanten

Die BFT-Konstanten werden als Bitflags verwendet, um verschiedene Dateitypen in einer Active Directory Domain Services identifizieren.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_BFT-PROTOKOLLVERZEICHNIS \_**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



Die Datei gehört zum Protokollverzeichnis.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_BFT-DATENBANKVERZEICHNIS \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



Die Datei gehört zum Datenbankverzeichnis.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_BFT-VERZEICHNIS**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Der angegebene Pfad ist ein Verzeichnis und kein Dateiname.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**\_BFT-PROTOKOLL**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Gibt eine Protokolldatei an, die zum Protokollverzeichnis gehört.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



Die Datei ist der Pfad des Protokollverzeichnisses.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ CHECKPOINT \_ DIR**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



Die Datei ist der Pfad des Prüfpunktverzeichnisses.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ \_ NTDS-DATENBANK**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



Die Datei ist eine Verzeichnisdienstdatenbank, die zum Datenbankverzeichnis gehört.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_BFT-PATCHDATEI \_**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



Die Datei ist eine Patchdatei, die zum Protokollverzeichnis gehört.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



Die Datei kann nicht erkannt werden. Die Datei stimmt nicht mit den bekannten Dateinamen und Dateitypen überein.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl> |



 

 





