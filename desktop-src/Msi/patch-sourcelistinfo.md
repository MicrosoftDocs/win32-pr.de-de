---
description: Die sourcelistinfo-Eigenschaft des Patch-Objekts Ruft die Quell Informations Eigenschaften für einen Patch ab und legt Sie fest. Diese Eigenschaft ruft msisourcelistgetinfo oder msisourcelist* tinfo auf. Dies ist eine Lese-oder Schreib Eigenschaft.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Patch. sourcelistinfo (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354070"
---
# <a name="patchsourcelistinfo-property"></a>Patch. sourcelistinfo (Eigenschaft)

Die **sourcelistinfo** -Eigenschaft des [**Patch**](patch-object.md) -Objekts Ruft die Quell Informations Eigenschaften für einen Patch ab und legt Sie fest. Diese Eigenschaft ruft [**msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) oder [**msisourcelist* tinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)auf. Dies ist eine Lese-oder Schreib Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Quell Informations Eigenschaften für einen Patch, der abgefragt oder festgelegt werden soll. Mögliche Werte finden Sie im Abschnitt "Hinweise" in diesem Thema.

## <a name="remarks"></a>Bemerkungen

Es können nicht alle Eigenschaften festgelegt werden, die abgerufen werden können. Der *szProperty* -Parameter kann einen der folgenden Werte aufweisen.



| Eigenschaft         | Kann festgelegt werden? | Bedeutung                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mediapackagepath | J        | Der Pfad relativ zum Stammverzeichnis des-Installationsmediums.                                                                                                                                                                                                          |
| Diskprompt       | J        | Die Eingabe Aufforderungs Vorlage, die verwendet wird, wenn der Benutzer zur Eingabe eines Installationsmediums                                                                                                                                                                                          |
| LastUsedSource   | J        | Der zuletzt verwendete Quell Speicherort für den Patch. Wenn Sie diese Eigenschaft festlegen, legen Sie den Quell Speicherort für eine Netzwerkquelle oder "u;" für den URL-Typ als Präfix für den Quell Speicherort fest. Verwenden Sie z. b. "n; \\ \\ Scratch Scratch- \\ \\ Test "oder" u; " https://microsoft.com/Patches/Office/SP1 . |
| Lastusedtype     | N        | "n", wenn die zuletzt verwendete Quelle ein Netzwerk Speicherort ist. "u", wenn die zuletzt verwendete Quelle ein URL-Speicherort war. "m", wenn die zuletzt verwendete Quelle Medien war. Leere Zeichenfolge (""), wenn keine zuletzt verwendete Quelle vorhanden ist.                                                                      |
| PackageName      | J        | Der Name des Windows Installer Pakets oder Patchpakets in der Quelle.                                                                                                                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**Msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**Msisourcelisteintinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




