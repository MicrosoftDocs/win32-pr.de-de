---
description: Die filesignatureinfo-Methode des Installer-Objekts nimmt den Pfad zu einer Datei an und gibt ein SafeArray von Bytes zurück, die den Hash oder das codierte Zertifikat darstellen.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Installer. filesignatureinfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355891"
---
# <a name="installerfilesignatureinfo-method"></a>Installer. filesignatureinfo-Methode

Die **filesignatureinfo** -Methode des [**Installer**](installer-object.md) -Objekts nimmt den Pfad zu einer Datei an und gibt ein SafeArray von Bytes zurück, die den Hash oder das codierte Zertifikat darstellen. Die Werte können dann verwendet werden, um die Tabellen [msidigitalsignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)und [msidigitalcertificate](msidigitalcertificate-table.md) aufzufüllen.

Weitere Informationen finden Sie unter dem [**SAFEARRAY-Datentyp**](/windows/win32/api/oaidl/ns-oaidl-safearray).

## <a name="syntax"></a>Syntax


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FilePath* 
</dt> <dd>

Vollständiger Pfad zu einer Datei, die digital signiert ist.

Beim Auffüllen der Tabellen [msidigitalsignature](msidigitalsignature-table.md) und [msidigitalcertificate](msidigitalcertificate-table.md) verweist *FilePath* auf eine Digital signierte CAB-Datei. Beim Auffüllen der [MsiPatchCertificate](msipatchcertificate-table.md) -und msidigitalcertificate-Tabellen zeigt *FilePath* auf einen digital signierten Patch.

</dd> <dt>

*Optionen* 
</dt> <dd>

Spezielle fehlerfallflags.



| Flag                                                                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msisignatureoptioninvalidhashfatal**</dt> <dt>1</dt> </dl> | Wenn die *Optionen* auf msisignatureoptioninvalidhashfatal festgelegt sind, gibt **filesignatureinfo** immer einen schwerwiegenden Fehler für einen ungültigen Hash zurück. <br/> Wenn die *Optionen* nicht auf msisignatureoptioninvalidhashfatal festgelegt sind und *Format* auf msiSignatureInfoCertificate festgelegt ist, gibt **filesignatureinfo** keinen Fehler für einen ungültigen Hash zurück.<br/> |



 

</dd> <dt>

*Format* 
</dt> <dd>

Die angeforderten Signatur Informationen.



| Flag                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Gibt ein SafeArray von Bytes zurück, die das codierte Zertifikat darstellen.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msisignatureinfohash**</dt> <dt>1</dt> </dl>                             | Gibt ein SafeArray von Bytes zurück, die den Hash darstellen.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt die Methode ein [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) von Bytes zurück, das entweder den Hash oder das codierte Zertifikat enthält.

## <a name="remarks"></a>Bemerkungen

Um eine vollständig verifizierte signierte Installation mithilfe von Automation zu erstellen, verwenden Sie die **filesignatureinfo** -Methode, um die Tabellen [msidigitalcertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)und [msidigitalsignature](msidigitalsignature-table.md) aufzufüllen. Weitere Informationen finden Sie unter [Erstellen einer vollständig verifizierten signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**Msigetfilesignatureinformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
