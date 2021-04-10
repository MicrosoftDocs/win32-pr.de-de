---
description: Aktualisiert die System-erneuerbarkeits Meldung (SRM) für High-Bandwidth Digital Content Protection (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215022"
---
# <a name="opm_set_hdcp_srm"></a>OPM \_ Set \_ HDCP \_ SRM

Aktualisiert die System-erneuerbarkeits Meldung (SRM) für High-Bandwidth Digital Content Protection (HDCP).



| Anforderung | Wert |
|--------------|-------------------------------------------------------------------------------------|
| Befehls-GUID | OPM \_ Set \_ HDCP \_ SRM                                                                 |
| Eingabedaten   | Eine [**OPM- \_ festgelegte \_ HDCP- \_ SRM- \_ Parameter**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) Struktur |



 

Der *pbadditionalparameters* -Parameter von [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) muss auf einen Puffer verweisen, der das SRM enthält. Das Format eines HDCP-SRM ist in der HDCP-Spezifikation dokumentiert. Legen Sie den *uladditionalparameterssize* -Parameter auf die Größe des Puffers (in Bytes) fest.

## <a name="remarks"></a>Bemerkungen

SRMs wird verwendet, um die Liste der gesperrten HDCP-Geräte zu aktualisieren. SRMs werden mit dem Videoinhalt geliefert.

Mit diesem Befehl wird das aktuelle SRM der Videoausgabe aktualisiert. Wenn HDCP zum Zeitpunkt des Befehls aktiviert ist, wird in der Videoausgabe das neue SRM verwendet, um zu überprüfen, ob eines der verbundenen HDCP-Geräte widerrufen wurde. Wenn die Videoausgabe ein gesperrtes Gerät erkennt, wird die Anzeige von Videos beendet. Wenn Sie diesen Befehl senden, während HDCP deaktiviert ist, wird der SRM in der Videoausgabe überprüft und gespeichert. Wenn die Anwendung HDCP später aktiviert, verwendet die Videoausgabe den neuen SRM, um den Sperr Status des Geräts zu überprüfen.

Dieser Befehl kann bewirken, dass die **configure** -Methode einen der folgenden Fehlercodes zurückgibt.



| Rückgabecode                                            | Beschreibung                             |
|--------------------------------------------------------|-----------------------------------------|
| Fehler \_ Grafik \_ OPM \_ ungültige \_ SRM-Datei                     | Der SRM ist ungültig.                   |
| Fehler \_ Grafik- \_ OPM- \_ Ausgabe \_ \_ \_ unterstützt \_ HDCP nicht | HDCP wird von der Videoausgabe nicht unterstützt. |



 

Dieser Befehl wird nicht unterstützt, wenn die **IOPMVideoOutput** -Schnittstelle das zertifizierte Output Protection Protocol (COPP) emuliert. Wenn die COPP-Semantik verwendet wird, ist die Anwendung für die Verarbeitung von SRMs und die Überprüfung des Sperr Status des HDCP-Geräts verantwortlich. Verwenden Sie die OPM-Anforderung zum Herstellen einer [ \_ \_ Verbindung mit dem \_ HDCP- \_ Geräte \_ Informations](opm-get-connected-hdcp-device-information.md) Status, um den Schlüsselauswahl Vektor (KSV) des Geräts zu erhalten, der zum Überprüfen des Sperr Status benötigt wird. Weitere Informationen zu SRMs finden Sie in der HDCP-Spezifikation.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM-Befehle](opm-commands.md)
</dt> </dl>

 

 




