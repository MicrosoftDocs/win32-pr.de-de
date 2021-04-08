---
title: IMAPIv1-Ergebnis Codes (imapierror. h)
description: Die Methoden der IMAPI-Schnittstellen geben S OK zurück, \_ Wenn die Methode erfolgreich war. Andernfalls geben Sie einen der folgenden Ergebnis Codes zurück.
ms.assetid: 0143ad10-9b65-4621-9bed-71dadd38c3fc
topic_type:
- apiref
api_name:
- IMAPI_S_PROPERTIESIGNORED
- IMAPI_S_BUFFER_TO_SMALL
- IMAPI_E_NOTOPENED
- IMAPI_E_NOTINITIALIZED
- IMAPI_E_USERABORT
- IMAPI_E_GENERIC
- IMAPI_E_MEDIUM_NOTPRESENT
- IMAPI_E_MEDIUM_INVALIDTYPE
- IMAPI_E_DEVICE_NOPROPERTIES
- IMAPI_E_DEVICE_NOTACCESSIBLE
- IMAPI_E_DEVICE_NOTPRESENT
- IMAPI_E_DEVICE_INVALIDTYPE
- IMAPI_E_INITIALIZE_WRITE
- IMAPI_E_INITIALIZE_ENDWRITE
- IMAPI_E_FILESYSTEM
- IMAPI_E_FILEACCESS
- IMAPI_E_DISCINFO
- IMAPI_E_TRACKNOTOPEN
- IMAPI_E_TRACKOPEN
- IMAPI_E_DISCFULL
- IMAPI_E_BADJOLIETNAME
- IMAPI_E_INVALIDIMAGE
- IMAPI_E_NOACTIVEFORMAT
- IMAPI_E_NOACTIVERECORDER
- IMAPI_E_WRONGFORMAT
- IMAPI_E_ALREADYOPEN
- IMAPI_E_WRONGDISC
- IMAPI_E_FILEEXISTS
- IMAPI_E_STASHINUSE
- IMAPI_E_DEVICE_STILL_IN_USE
- IMAPI_E_LOSS_OF_STREAMING
- IMAPI_E_COMPRESSEDSTASH
- IMAPI_E_ENCRYPTEDSTASH
- IMAPI_E_NOTENOUGHDISKFORSTASH
- IMAPI_E_REMOVABLESTASH
- IMAPI_E_CANNOT_WRITE_TO_MEDIA
- IMAPI_E_TRACK_NOT_BIG_ENOUGH
api_location:
- Imapierror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80e8aba2a2d3d12628a45c6716c6f94a405d752f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739984"
---
# <a name="imapiv1-result-codes"></a>IMAPIv1-Ergebnis Codes

Die Methoden der IMAPI-Schnittstellen geben S OK zurück, \_ Wenn die Methode erfolgreich war. Andernfalls geben Sie einen der folgenden Ergebnis Codes zurück.



| Konstante/Wert                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMAPI_S_PROPERTIESIGNORED"></span><span id="imapi_s_propertiesignored"></span><dl> <dt>**IMAPI \_ S \_ propertiesignored**</dt> <dt>0x40200</dt> </dl>                   | Eine unbekannte Eigenschaft wurde in einem Eigenschaften Satz übermittelt und wurde ignoriert.<br/>                                                                                                                                                                              |
| <span id="IMAPI_S_BUFFER_TO_SMALL"></span><span id="imapi_s_buffer_to_small"></span><dl> <dt>**IMAPI \_ S- \_ Puffer \_ zu \_ kleiner**</dt> <dt>0x40201</dt> </dl>                       | Der Ausgabepuffer ist zu klein.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTOPENED"></span><span id="imapi_e_notopened"></span><dl> <dt>**IMAPI \_ E \_ notgeöffnet**</dt> <dt>0x8004020b</dt> </dl>                                        | Ein [**idiscmaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) -Befehl wurde nicht durchgeführt.<br/>                                                                                                                                                                        |
| <span id="IMAPI_E_NOTINITIALIZED"></span><span id="imapi_e_notinitialized"></span><dl> <dt>**IMAPI \_ E \_ notinitialized**</dt> <dt>0x8004020c</dt> </dl>                         | Ein Aufzeichnungs Objekt wurde nicht initialisiert.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_USERABORT"></span><span id="imapi_e_userabort"></span><dl> <dt>**IMAPI \_ E \_ userabort**</dt> <dt>0x8004020D</dt> </dl>                                        | Der Benutzer hat den Vorgang abgebrochen.<br/>                                                                                                                                                                                                                  |
| <span id="IMAPI_E_GENERIC"></span><span id="imapi_e_generic"></span><dl> <dt>**IMAPI \_ E \_ Generic**</dt> <dt>0x8004020e</dt> </dl>                                              | Ein generischer Fehler ist aufgetreten.<br/>                                                                                                                                                                                                                         |
| <span id="IMAPI_E_MEDIUM_NOTPRESENT"></span><span id="imapi_e_medium_notpresent"></span><dl> <dt>**IMAPI \_ E \_ Medium \_ notpresent**</dt> <dt>0x8004020f</dt> </dl>               | Es ist kein Laufwerk im Gerät vorhanden.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_MEDIUM_INVALIDTYPE"></span><span id="imapi_e_medium_invalidtype"></span><dl> <dt>**IMAPI \_ E \_ Mittel \_ invalidtype**</dt> <dt>0x80040210</dt> </dl>            | Das Medium ist kein Typ, der verwendet werden kann.<br/>                                                                                                                                                                                                         |
| <span id="IMAPI_E_DEVICE_NOPROPERTIES"></span><span id="imapi_e_device_noproperties"></span><dl> <dt>**IMAPI \_ E- \_ Gerät \_ noproperties**</dt> <dt>0x80040211</dt> </dl>         | Die Aufzeichnung unterstützt keine Eigenschaften.<br/>                                                                                                                                                                                                     |
| <span id="IMAPI_E_DEVICE_NOTACCESSIBLE"></span><span id="imapi_e_device_notaccessible"></span><dl> <dt>**IMAPI \_ E \_ Gerät nicht \_ zugänglich**</dt> <dt>0x80040212</dt> </dl>      | Das Gerät kann nicht verwendet werden oder wird bereits verwendet.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DEVICE_NOTPRESENT"></span><span id="imapi_e_device_notpresent"></span><dl> <dt>**IMAPI \_ E \_ Gerät \_ notpresent**</dt> <dt>0x80040213</dt> </dl>               | Das Gerät ist nicht vorhanden oder wurde entfernt.<br/>                                                                                                                                                                                                    |
| <span id="IMAPI_E_DEVICE_INVALIDTYPE"></span><span id="imapi_e_device_invalidtype"></span><dl> <dt>**IMAPI \_ E \_ Device \_ invalidtype**</dt> <dt>0x80040214</dt> </dl>            | Der Recorder unterstützt keinen Vorgang.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_INITIALIZE_WRITE"></span><span id="imapi_e_initialize_write"></span><dl> <dt>**IMAPI \_ E " \_ \_ Write**</dt> <dt>0x80040215</dt> " Initialisieren </dl>                  | Die Laufwerk Schnittstelle konnte nicht zum Schreiben initialisiert werden.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_INITIALIZE_ENDWRITE"></span><span id="imapi_e_initialize_endwrite"></span><dl> <dt>**IMAPI \_ E \_ Initialisieren von \_ EndWrite**</dt> <dt>0x80040216</dt> </dl>         | Die Laufwerk Schnittstelle konnte nicht zum Schließen initialisiert werden.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_FILESYSTEM"></span><span id="imapi_e_filesystem"></span><dl> <dt>**IMAPI \_ E \_ File System**</dt> <dt>0x80040217</dt> </dl>                                     | Fehler beim Aktivieren/Deaktivieren des Dateisystem Zugriffs oder bei der automatischen Einfügungs Erkennung.<br/>                                                                                                                                                 |
| <span id="IMAPI_E_FILEACCESS"></span><span id="imapi_e_fileaccess"></span><dl> <dt>**IMAPI \_ E \_ FileAccess**</dt> <dt>0x80040218</dt> </dl>                                     | Fehler beim Schreiben der Bilddatei.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DISCINFO"></span><span id="imapi_e_discinfo"></span><dl> <dt>**IMAPI \_ E \_ discinfo**</dt> <dt>0x80040219</dt> </dl>                                           | Fehler beim Lesen von Festplattendaten vom Gerät.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_TRACKNOTOPEN"></span><span id="imapi_e_tracknotopen"></span><dl> <dt>**IMAPI \_ E \_ tracknotopen**</dt> <dt>0x8004021a</dt> </dl>                               | Eine Audiospur ist nicht zum Schreiben geöffnet.<br/>                                                                                                                                                                                                           |
| <span id="IMAPI_E_TRACKOPEN"></span><span id="imapi_e_trackopen"></span><dl> <dt>**IMAPI \_ E \_ trackopen**</dt> <dt>0x8004021b</dt> </dl>                                        | Eine geöffnete Audiospur wird bereits bereitgestellt.<br/>                                                                                                                                                                                                      |
| <span id="IMAPI_E_DISCFULL"></span><span id="imapi_e_discfull"></span><dl> <dt>**IMAPI \_ E \_ DISCFULL**</dt> <dt>0x8004021c</dt> </dl>                                           | Die Festplatte kann keine weiteren Daten enthalten.<br/>                                                                                                                                                                                                               |
| <span id="IMAPI_E_BADJOLIETNAME"></span><span id="imapi_e_badjolietname"></span><dl> <dt>**IMAPI \_ E \_ badjolietname**</dt> <dt>0x8004021d</dt> </dl>                            | Die Anwendung hat versucht, ein Element mit ungültigem Namen zu einem Laufwerk hinzuzufügen.<br/>                                                                                                                                                                                     |
| <span id="IMAPI_E_INVALIDIMAGE"></span><span id="imapi_e_invalidimage"></span><dl> <dt>**IMAPI \_ E \_ invalidimage**</dt> <dt>0x8004021e</dt> </dl>                               | Das gestaffelte Image ist für einen Burn nicht geeignet. Sie wurde beschädigt oder gelöscht und verfügt über keinen verwendbaren Inhalt.<br/>                                                                                                                                          |
| <span id="IMAPI_E_NOACTIVEFORMAT"></span><span id="imapi_e_noactiveformat"></span><dl> <dt>**IMAPI \_ E \_ noactiveformat**</dt> <dt>0x8004021f</dt> </dl>                         | Es wurde kein aktiver Format Master mithilfe von [**idiscmaster::**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscmasterformat)Abbild Format ausgewählt.<br/>                                                                                                      |
| <span id="IMAPI_E_NOACTIVERECORDER"></span><span id="imapi_e_noactiverecorder"></span><dl> <dt>**IMAPI \_ E \_ noactiverecorder**</dt> <dt>0x80040220</dt> </dl>                   | Es wurde keine Active Disk Recorder mithilfe von [**idiscmaster:: setactivediscrecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder)ausgewählt.<br/>                                                                                                              |
| <span id="IMAPI_E_WRONGFORMAT"></span><span id="imapi_e_wrongformat"></span><dl> <dt>**IMAPI \_ E-Fehler \_ formatieren**</dt> <dt>0x80040221</dt> </dl>                                  | Es wurde ein [**ijolietdiscmaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) -Rückruf erstellt, wenn [**iredbookdiscmaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) das aktive Format oder umgekehrt ist. Um ein anderes Format zu verwenden, ändern Sie das Format, und löschen Sie den Bilddatei-Inhalt.<br/> |
| <span id="IMAPI_E_ALREADYOPEN"></span><span id="imapi_e_alreadyopen"></span><dl> <dt>**IMAPI \_ E \_ Al:yopen**</dt> <dt>0x80040222</dt> </dl>                                  | Es wurde bereits ein [**idiscmaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) -Aufrufe für dieses Objekt von Ihrer Anwendung durchgeführt.<br/>                                                                                                                            |
| <span id="IMAPI_E_WRONGDISC"></span><span id="imapi_e_wrongdisc"></span><dl> <dt>**IMAPI \_ E \_**</dt> Fehler bei <dt>0x80040223</dt> </dl>                                        | Der Datenträger für die IMAPI-mehrfach Sitzung wurde aus dem aktiven Recorder entfernt.<br/>                                                                                                                                                                           |
| <span id="IMAPI_E_FILEEXISTS"></span><span id="imapi_e_fileexists"></span><dl> <dt>**IMAPI \_ E \_ fileexistiert**</dt> <dt>0x80040224</dt> </dl>                                     | Die hinzu zufügende Datei befindet sich bereits in der Bilddatei, und das überschreibungsflag wurde nicht festgelegt.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_STASHINUSE"></span><span id="imapi_e_stashinuse"></span><dl> <dt>**IMAPI \_ E \_ stashinuse**</dt> <dt>0x80040225</dt> </dl>                                     | Eine andere Anwendung verwendet bereits die IMAPI Stash-Datei, die zum Bereitstellen eines Festplatten Abbilds erforderlich ist. Versuchen Sie es später noch einmal.<br/>                                                                                                                                        |
| <span id="IMAPI_E_DEVICE_STILL_IN_USE"></span><span id="imapi_e_device_still_in_use"></span><dl> <dt>**IMAPI \_ E- \_ Gerät wird \_ weiterhin \_ \_ verwendet**</dt> <dt>0x80040226</dt> </dl>       | Dieses Gerät wird bereits von einer anderen Anwendung verwendet, sodass IMAPI nicht auf das Gerät zugreifen kann.<br/>                                                                                                                                                              |
| <span id="IMAPI_E_LOSS_OF_STREAMING"></span><span id="imapi_e_loss_of_streaming"></span><dl> <dt>**IMAPI \_ E- \_ Verlust \_ des \_ Streamings**</dt> <dt>0x80040227</dt> </dl>              | Das Streamen von Inhalten ist verloren gegangen. Möglicherweise ist ein Puffer unter dem Testlauf aufgetreten.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_COMPRESSEDSTASH"></span><span id="imapi_e_compressedstash"></span><dl> <dt>**IMAPI \_ E \_ compressedstash**</dt> <dt>0x80040228</dt> </dl>                      | Der Stash befindet sich auf einem komprimierten Volume und kann nicht gelesen werden.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_ENCRYPTEDSTASH"></span><span id="imapi_e_encryptedstash"></span><dl> <dt>**IMAPI \_ E \_ verschlüsseltedstash**</dt> <dt>0x80040229</dt> </dl>                         | Der Stash befindet sich auf einem verschlüsselten Volume und kann nicht gelesen werden.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTENOUGHDISKFORSTASH"></span><span id="imapi_e_notenoughdiskforstash"></span><dl> <dt>**IMAPI \_ E \_ notenoughdiskforstash**</dt> <dt>0x8004022a</dt> </dl>    | Es ist nicht genügend freier Speicherplatz vorhanden, um die Stash-Datei auf dem angegebenen Volume zu erstellen.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_REMOVABLESTASH"></span><span id="imapi_e_removablestash"></span><dl> <dt>**IMAPI \_ E \_ removablestash**</dt> <dt>0x8004022b</dt> </dl>                         | Der ausgewählte Stash-Speicherort befindet sich auf einem Wechselmedium.<br/>                                                                                                                                                                                              |
| <span id="IMAPI_E_CANNOT_WRITE_TO_MEDIA"></span><span id="imapi_e_cannot_write_to_media"></span><dl> <dt>**IMAPI \_ E \_ kann \_ nicht \_ in \_ Medien**</dt> <dt>0x8004022c</dt> schreiben </dl> | Auf das Medium kann nicht geschrieben werden.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_TRACK_NOT_BIG_ENOUGH"></span><span id="imapi_e_track_not_big_enough"></span><dl> <dt>**IMAPI \_ E \_ Track \_ nicht \_ groß \_ genug**</dt> <dt>0x8004022d</dt> </dl>    | Der Titel ist nicht groß genug.<br/>                                                                                                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Imapierror. h</dt> </dl> |



 

 





