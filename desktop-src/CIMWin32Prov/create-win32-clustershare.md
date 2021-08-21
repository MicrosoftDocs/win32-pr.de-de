---
description: Erstellt eine neue Win32 \_ ClusterShare-Instanz.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Create-Methode der Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: edaafa00f792cf01b4166d525171cf15b7f781c8c0c943c17377b3bd9b3401dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020588"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Create-Methode der Win32 \_ ClusterShare-Klasse

Erstellt eine neue [**Win32 \_ ClusterShare-Instanz.**](win32-clustershare.md)

## <a name="syntax"></a>Syntax


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ In\]
</dt> <dd>

Lokaler Pfad der Windows Freigabe.

Beispiel: "C: \\ Programme".

</dd> <dt>

*Name* \[ In\]
</dt> <dd>

Der Alias für einen Pfad, der als Freigabe auf einem Computersystem mit Windows eingerichtet ist.

Beispiel: "public".

</dd> <dt>

*Typ* \[ In\]
</dt> <dd>

Typ der Ressource, die freigegeben wird. Zu den Typen gehören Datenträgerlaufwerke, Druckwarteschlangen, prozessübergreifende Kommunikation (Interprocess Communications, IPC) und allgemeine Geräte.

<dt>

0 (0x0)
</dt> <dd>

Laufwerk

</dd> <dt>

1 (0x1)
</dt> <dd>

Druckwarteschlange

</dd> <dt>

2 (0x2)
</dt> <dd>

Gerät

</dd> <dt>

3 (0x3)
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000)
</dt> <dd>

Datenträgerlaufwerkadministrator

</dd> <dt>

2147483649 (0x80000001)
</dt> <dd>

Druckwarteschlangenadministrator

</dd> <dt>

2147483650 (0x80000002)
</dt> <dd>

Geräteadministrator

</dd> <dt>

2147483651 (0x80000003)
</dt> <dd>

IPC-Administrator

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ in, optional\]
</dt> <dd>

Begrenzen Sie die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.

</dd> <dt>

*Beschreibung* \[ in, optional\]
</dt> <dd>

Eine Beschreibung des Objekts.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

TBD

</dd> <dt>

*Zugriff* \[ in, optional\]
</dt> <dd>

Optionale eingebettete Instanz einer [**Win32 \_ SecurityDescriptor-Klasse,**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) die den Sicherheitsdeskriptor für die neue Freigabe enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ ClusterShare**](win32-clustershare.md)
</dt> </dl>

 

