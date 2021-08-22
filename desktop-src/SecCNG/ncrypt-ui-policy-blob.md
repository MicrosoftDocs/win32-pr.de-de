---
description: Wird mit der NCRYPT \_ UI \_ POLICY \_ PROPERTY-Eigenschaft verwendet, um Benutzeroberflächeninformationen für einen Schlüssel zu enthalten.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: NCRYPT_UI_POLICY_BLOB -Struktur (Ncrypt \_ provider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: 21f9f6c0f6956ffa89da45c9dcd23727c0b3cea2d4f31131713f9ed5a0c3a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907600"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>NCRYPT \_ UI POLICY BLOB structure (NCRYPT-UI-RICHTLINIEN-BLOB-Struktur) \_ \_

Die **NCRYPT \_ UI POLICY \_ \_ BLOB-Struktur** wird mit der [**NCRYPT \_ UI POLICY \_ \_ PROPERTY-Eigenschaft**](key-storage-property-identifiers.md) verwendet, um Benutzeroberflächeninformationen für einen Schlüssel zu enthalten.

## <a name="syntax"></a>Syntax


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Die Versionsnummer der -Struktur. Dieser Member muss 1 enthalten.

</dd> <dt>

**dwFlags**
</dt> <dd>

Eine Gruppe von Flags, die zusätzliche Informationen zur Benutzeroberfläche oder Anforderungen bereitstellen.



| Wert                                                                                                                                                                                                                                                                                                  | Bedeutung                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_ FLAG \_ FÜR \_ \_ BENUTZEROBERFLÄCHENSCHUTZSCHLÜSSEL**</dt> <dt>0X00000001</dt> </dl>                                | Zeigen Sie die Benutzeroberfläche mit starkem Schlüssel nach Bedarf an.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_ FLAG \_ "UI FORCE \_ HIGH \_ \_ PROTECTION 0X00000002**</dt> <dt></dt> </dl> | Erzwingen sie einen hohen Schutz.<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

Die Länge des Erstellungstitels in Bytes. Der Erstellungstitel ist eine unicode-Zeichenfolge mit NULL-Terminierung, die den Text angibt, der beim Abschluss des Schlüssels als Titel des Dialogfelds mit starkem Schlüssel verwendet wird. Der Erstellungstitel muss unmittelbar nach der **NCRYPT \_ UI \_ POLICY \_ BLOB-Struktur platziert** werden. Wenn der Wert des **cbCreationTitle-Members** auf 0 festgelegt ist, wird ein Standarderstellungstitel für den Titel des Dialogfelds mit starkem Schlüssel verwendet. Dieser Member wird nur bei der Schlüssel finalisierung verwendet.

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

Die Länge des Angezeigtnamens des Schlüssels in Bytes. Der Anzeigename ist eine auf NULL terminierte Unicode-Zeichenfolge, die den Text enthält, der im Dialogfeld mit starkem Schlüssel als Name des Schlüssels angezeigt wird. Der Benutzerfreundlichname muss unmittelbar nach dem Erstellungstitel in diesem BLOB platziert werden. Wenn der Wert des **cbFriendlyName-Mitglieds** auf 0 festgelegt ist, wird im Dialogfeld mit starkem Schlüssel ein Standardname verwendet. Dieser Member wird sowohl beim Abschluss des Schlüssels als auch beim Verwenden des Schlüssels verwendet.

</dd> <dt>

**cbDescription**
</dt> <dd>

Die Länge der Schlüsselbeschreibung in Bytes. Die Schlüsselbeschreibung ist eine auf NULL terminierte Unicode-Zeichenfolge, die den Text enthält, der im Dialogfeld mit starkem Schlüssel als Beschreibung des Schlüssels angezeigt wird. Der Beschreibungswert muss unmittelbar nach dem Angezeigten in diesem BLOB platziert werden. Wenn der Wert des **cbDescription-Mitglieds** auf 0 festgelegt ist, wird im Dialogfeld mit starkem Schlüssel eine Standardbeschreibung verwendet. Dieser Member wird sowohl beim Abschluss des Schlüssels als auch beim Verwenden des Schlüssels verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist im Header Ncrypt \_ provider.h enthalten. Um die -Struktur zu verwenden, müssen Sie das [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) von Microsoft Verbinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                          |
| Header<br/>                   | <dl> <dt>Ncrypt \_ provider.h</dt> </dl> |



 

