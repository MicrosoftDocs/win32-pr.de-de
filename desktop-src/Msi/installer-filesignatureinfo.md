---
description: Die FileSignatureInfo-Methode des Installer-Objekts nimmt den Pfad zu einer Datei und gibt ein SAFEARRAY von Bytes zurück, die den Hash oder das codierte Zertifikat darstellen.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Installer.FileSignatureInfo-Methode
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
ms.openlocfilehash: 670b5ba6deb4a53429180e832c2a49e4968c53efbe7c54cdf50e62e20bf5503b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630781"
---
# <a name="installerfilesignatureinfo-method"></a>Installer.FileSignatureInfo-Methode

Die **FileSignatureInfo-Methode** des [**Installer-Objekts**](installer-object.md) nimmt den Pfad zu einer Datei und gibt ein SAFEARRAY von Bytes zurück, die den Hash oder das codierte Zertifikat darstellen. Die Werte können dann verwendet werden, um die Tabellen [MsiDigitalSignature,](msidigitalsignature-table.md) [MsiPatchCertificate](msipatchcertificate-table.md)und [MsiDigitalCertificate zu](msidigitalcertificate-table.md) füllen.

Weitere Informationen finden Sie unter [**SAFEARRAY-Datentyp.**](/windows/win32/api/oaidl/ns-oaidl-safearray)

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

*Filepath* 
</dt> <dd>

Vollständiger Pfad zu einer Datei, die digital signiert ist.

Beim Aufstellen der [Tabellen MsiDigitalSignature](msidigitalsignature-table.md) und [MsiDigitalCertificate](msidigitalcertificate-table.md) verweist *FilePath* auf ein digital signiertes Schränkchen. Beim Aufstellen der [Tabellen MsiPatchCertificate](msipatchcertificate-table.md) und MsiDigitalCertificate verweist *FilePath* auf einen digital signierten Patch.

</dd> <dt>

*Optionen* 
</dt> <dd>

Spezielle Fehlerfallflags.



| Flag                                                                                                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Wenn *Optionen* auf msiSignatureOptionInvalidHashFatal festgelegt sind, gibt **FileSignatureInfo** immer einen schwerwiegenden Fehler für einen ungültigen Hash zurück. <br/> Wenn *Options* nicht auf msiSignatureOptionInvalidHashFatal und *Format* auf msiSignatureInfoCertificate festgelegt ist, gibt **FileSignatureInfo** keinen Fehler für einen ungültigen Hash zurück.<br/> |



 

</dd> <dt>

*Format* 
</dt> <dd>

Die angeforderten Signaturinformationen.



| Flag                                                                                                                                                                                                                                                                                                        | Bedeutung                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Gibt ein SAFEARRAY von Bytes zurück, die das codierte Zertifikat darstellen.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Gibt ein SAFEARRAY von Bytes zurück, die den Hash darstellen.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt die Methode [safearray](/windows/win32/api/oaidl/ns-oaidl-safearray) von Bytes zurück, die entweder das Hashzertifikat oder das codierte Zertifikat enthalten.

## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erstellen einer vollständig überprüften signierten Installation mithilfe der Automatisierung die **FileSignatureInfo-Methode,** um die Tabellen [MsiDigitalCertificate,](msidigitalcertificate-table.md) [MsiPatchCertificate](msipatchcertificate-table.md)und [MsiDigitalSignature](msidigitalsignature-table.md) zu füllen. Weitere Informationen finden Sie unter [Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation.](authoring-a-fully-verified-signed-installation-using-automation.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
