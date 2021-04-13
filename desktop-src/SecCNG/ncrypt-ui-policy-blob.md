---
description: Wird mit der Eigenschaften Eigenschaft der UI-Richtlinie der NCrypt verwendet \_ \_ \_ , um Benutzeroberflächen Informationen für einen Schlüssel zu enthalten.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: NCRYPT_UI_POLICY_BLOB Struktur (NCrypt \_ Provider. h)
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
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528727"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>Ncrypt- \_ UI- \_ Richtlinien- \_ BLOB-Struktur

Die NCrypt-benutzeroberflächenrichtlinienblob-Struktur wird mit der [**Eigenschaften Eigenschaft NCrypt \_ UI- \_ Richtlinie \_**](key-storage-property-identifiers.md) verwendet, um Benutzeroberflächen Informationen für einen Schlüssel zu enthalten **\_ \_ \_**

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

Die Versionsnummer der-Struktur. Dieser Member muss 1 enthalten.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ein Satz von Flags, die zusätzliche Informationen oder Anforderungen an die Benutzeroberfläche bereitstellen.



| Wert                                                                                                                                                                                                                                                                                                  | Bedeutung                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCrypt \_ UI \_ Protect \_ Key- \_ Flag**</dt> <dt>0x00000001</dt> </dl>                                | Zeigen Sie die Benutzeroberfläche mit starkem Schlüssel nach Bedarf an.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCrypt \_ \_ \_ \_ \_ Flag**</dt> für die Benutzeroberflächen-Force-Schutz <dt>0x00000002</dt> </dl> | Erzwingen Sie einen hohen Schutz.<br/>                           |



 

</dd> <dt>

**cbkreationtitle**
</dt> <dd>

Die Länge (in Byte) des Erstellungs Titels. Der Erstellungs Titel ist eine auf NULL endende Unicode-Zeichenfolge, die den Text angibt, der als Titel des Dialog Felds für den starken Schlüssel verwendet wird, wenn der Schlüssel abgeschlossen ist. Der Erstellungs Titel muss direkt nach der **blobstruktur der NCrypt- \_ UI- \_ Richtlinie \_** platziert werden. Wenn der Wert des **cbkreationtitle** -Members auf 0 festgelegt ist, wird ein standardmäßiger Erstellungs Titel für den Titel des Dialog Felds für den starken Schlüssel verwendet. Dieser Member wird nur bei der Schlüssel Finalisierung verwendet.

</dd> <dt>

**cbfriendlyname**
</dt> <dd>

Die Länge (in Byte) des anzeigen Amens des Schlüssels. Der Anzeige Name ist eine NULL-terminierte Unicode-Zeichenfolge, die den Text enthält, der im Dialogfeld für den starken Schlüssel als Name des Schlüssels angezeigt wird. Der Anzeige Name muss direkt nach dem Erstellungs Titel in diesem BLOB platziert werden. Wenn der Wert des Members **cbfriendlyname** auf 0 festgelegt ist, wird im Dialogfeld für den starken Schlüssel ein Standardname verwendet. Dieser Member wird sowohl verwendet, wenn der Schlüssel abgeschlossen ist, als auch, wenn der Schlüssel verwendet wird.

</dd> <dt>

**cbdescription**
</dt> <dd>

Die Länge (in Byte) der Schlüssel Beschreibung. Die Schlüssel Beschreibung ist eine mit NULL endenden Unicode-Zeichenfolge, die den Text enthält, der im Dialogfeld für den starken Schlüssel als die Beschreibung des Schlüssels angezeigt wird. Der Beschreibungs Wert muss direkt nach dem anzeigen Amen in diesem BLOB eingefügt werden. Wenn der Wert des **cbdescription** -Members auf 0 festgelegt ist, wird im Dialogfeld für den starken Schlüssel eine Standardbeschreibung verwendet. Dieser Member wird sowohl verwendet, wenn der Schlüssel abgeschlossen ist, als auch, wenn der Schlüssel verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist im NCrypt \_ Provider. h-Header enthalten. Um die Struktur zu verwenden, müssen Sie das [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) von Microsoft Connect herunterladen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                          |
| Header<br/>                   | <dl> <dt>Ncrypt- \_ Anbieter. h</dt> </dl> |



 

